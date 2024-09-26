# `module Random`

Mersenne Twister, ported to Fix Language by https://github.com/pt9999.

# Types and aliases

## `namespace Random`

### `type Random = unbox struct { ...fields... }`

Random number generator.

#### field `mt : Std::Array Std::U64`

#### field `mti : Std::I64`

# Traits and aliases

# Trait implementations

# Values

## `namespace Random`

### `_LM : Std::U64`

### `_MATRIX_A : Std::U64`

### `_MM : Std::I64`

### `_NN : Std::I64`

### `_UM : Std::U64`

### `_mag01 : Std::Array Std::U64`

### `generate_F64 : Random::Random -> (Random::Random, Std::F64)`

Generates a random number on [0, 1]-real-interval.

### `generate_F64_2 : Random::Random -> (Random::Random, Std::F64)`

Generates a random number on [0, 1)-real-interval.

### `generate_F64_3 : Random::Random -> (Random::Random, Std::F64)`

Generates a random number on (0, 1)-real-interval.

### `generate_I64_nonneg : Random::Random -> (Random::Random, Std::I64)`

Generates a random number on [0, 2^63-1]-interval.

### `generate_U64 : Random::Random -> (Random::Random, Std::U64)`

Generates a random number on [0, 2^64-1]-interval.

### `init_by_array : Std::Array Std::U64 -> Random::Random`

Initializes `Random` with an array.

### `init_by_seed : Std::U64 -> Random::Random`

Initializes `Random` with a seed.

## `namespace Random::Random`

### `@mt : Random::Random -> Std::Array Std::U64`

Retrieves the field `mt` from a value of `Random`.

### `@mti : Random::Random -> Std::I64`

Retrieves the field `mti` from a value of `Random`.

### `act_mt : [f : Std::Functor] (Std::Array Std::U64 -> f (Std::Array Std::U64)) -> Random::Random -> f Random::Random`

Updates a value of `Random` by applying a functorial action to field `mt`.

### `act_mti : [f : Std::Functor] (Std::I64 -> f Std::I64) -> Random::Random -> f Random::Random`

Updates a value of `Random` by applying a functorial action to field `mti`.

### `mod_mt : (Std::Array Std::U64 -> Std::Array Std::U64) -> Random::Random -> Random::Random`

Updates a value of `Random` by applying a function to field `mt`.

### `mod_mti : (Std::I64 -> Std::I64) -> Random::Random -> Random::Random`

Updates a value of `Random` by applying a function to field `mti`.

### `set_mt : Std::Array Std::U64 -> Random::Random -> Random::Random`

Updates a value of `Random` by setting field `mt` to a specified one.

### `set_mti : Std::I64 -> Random::Random -> Random::Random`

Updates a value of `Random` by setting field `mti` to a specified one.