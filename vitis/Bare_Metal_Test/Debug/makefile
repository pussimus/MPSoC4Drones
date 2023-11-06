################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
ELFSIZE += \
Bare_Metal_Test.elf.size \


# All Target
all: Bare_Metal_Test.elf secondary-outputs

# Tool invocations
Bare_Metal_Test.elf: $(OBJS) ../src/lscript.ld $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: ARM v8 gcc linker'
	aarch64-none-elf-gcc -Wl,-T -Wl,../src/lscript.ld -L/home/magnus/workspace/u96v2_sbc_mp4d/export/u96v2_sbc_mp4d/sw/u96v2_sbc_mp4d/standalone_psu_cortexa53_0/bsplib/lib -o "Bare_Metal_Test.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

Bare_Metal_Test.elf.size: Bare_Metal_Test.elf
	@echo 'Invoking: ARM v8 Print Size'
	aarch64-none-elf-size Bare_Metal_Test.elf  |tee "Bare_Metal_Test.elf.size"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(S_UPPER_DEPS)$(C_DEPS)$(ELFSIZE) Bare_Metal_Test.elf
	-@echo ' '

secondary-outputs: $(ELFSIZE)

.PHONY: all clean dependents

-include ../makefile.targets
