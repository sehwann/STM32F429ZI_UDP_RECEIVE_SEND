################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (11.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/LwIP/src/netif/ppp/subdir.mk
-include Middlewares/Third_Party/LwIP/src/netif/subdir.mk
-include Middlewares/Third_Party/LwIP/src/core/ipv6/subdir.mk
-include Middlewares/Third_Party/LwIP/src/core/ipv4/subdir.mk
-include Middlewares/Third_Party/LwIP/src/core/subdir.mk
-include Middlewares/Third_Party/LwIP/src/apps/mqtt/subdir.mk
-include Middlewares/Third_Party/LwIP/src/api/subdir.mk
-include LWIP/Target/subdir.mk
-include LWIP/App/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Drivers/BSP/Components/lan8742/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Nucleo_F429ZI_UDP_SEND
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Nucleo_F429ZI_UDP_SEND.elf \

MAP_FILES += \
Nucleo_F429ZI_UDP_SEND.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Nucleo_F429ZI_UDP_SEND.list \


# All Target
all: main-build

# Main-build Target
main-build: Nucleo_F429ZI_UDP_SEND.elf secondary-outputs

# Tool invocations
Nucleo_F429ZI_UDP_SEND.elf Nucleo_F429ZI_UDP_SEND.map: $(OBJS) $(USER_OBJS) C:\Users\PETABREW001\STM32CubeIDE\workspace_1.13.1\Nucleo_F429ZI_UDP_SEND\STM32F429ZITX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Nucleo_F429ZI_UDP_SEND.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\PETABREW001\STM32CubeIDE\workspace_1.13.1\Nucleo_F429ZI_UDP_SEND\STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Nucleo_F429ZI_UDP_SEND.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Nucleo_F429ZI_UDP_SEND.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Nucleo_F429ZI_UDP_SEND.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Nucleo_F429ZI_UDP_SEND.elf Nucleo_F429ZI_UDP_SEND.list Nucleo_F429ZI_UDP_SEND.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
