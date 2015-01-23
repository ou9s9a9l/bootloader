################################################################################
# Automatically-generated file. Do not edit!
################################################################################

SHELL := cmd.exe
RM := rm -rf

USER_OBJS :=

LIBS := 
PROJ := 

O_SRCS := 
C_SRCS := 
S_SRCS := 
S_UPPER_SRCS := 
OBJ_SRCS := 
ASM_SRCS := 
PREPROCESSING_SRCS := 
OBJS := 
OBJS_AS_ARGS := 
C_DEPS := 
C_DEPS_AS_ARGS := 
EXECUTABLES := 
OUTPUT_FILE_PATH :=
OUTPUT_FILE_PATH_AS_ARGS :=
AVR_APP_PATH :=$$$AVR_APP_PATH$$$
QUOTE := "
ADDITIONAL_DEPENDENCIES:=
OUTPUT_FILE_DEP:=
LIB_DEP:=

# Every subdirectory with source files must be described here
SUBDIRS := 


# Add inputs and outputs from these tool invocations to the build variables 
C_SRCS +=  \
../bootldr.c


PREPROCESSING_SRCS += 


ASM_SRCS += 


OBJS +=  \
bootldr.o

OBJS_AS_ARGS +=  \
bootldr.o

C_DEPS +=  \
bootldr.d

C_DEPS_AS_ARGS +=  \
bootldr.d

OUTPUT_FILE_PATH +=Bootldr.elf

OUTPUT_FILE_PATH_AS_ARGS +=Bootldr.elf

ADDITIONAL_DEPENDENCIES:=

OUTPUT_FILE_DEP:= ./makedep.mk

LIB_DEP+= 

# AVR32/GNU C Compiler



./%.o: .././%.c
	@echo Building file: $<
	@echo Invoking: AVR/GNU C Compiler : 0.0.0
	$(QUOTE)d:\WinAVR\bin\avr-gcc.exe$(QUOTE)  -x c -Os -ffunction-sections -fdata-sections -Wall -mmcu=atmega644p -c -gdwarf-2 -fsigned-char -MD -MP -MF "$(@:%.o=%.d)" -MT"$(@:%.o=%.d)" -MT"$(@:%.o=%.o)"   -o "$@" "$<" 
	@echo Finished building: $<
	



# AVR32/GNU Preprocessing Assembler



# AVR32/GNU Assembler




ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: $(OUTPUT_FILE_PATH) $(ADDITIONAL_DEPENDENCIES)

$(OUTPUT_FILE_PATH): $(OBJS) $(USER_OBJS) $(OUTPUT_FILE_DEP) $(LIB_DEP)
	@echo Building target: $@
	@echo Invoking: AVR/GNU Linker : 0.0.0
	$(QUOTE)d:\WinAVR\bin\avr-gcc.exe$(QUOTE) -o$(OUTPUT_FILE_PATH_AS_ARGS) $(OBJS_AS_ARGS) $(USER_OBJS) $(LIBS) -Wl,-Map="Bootldr.map" -Wl,--start-group  -Wl,--end-group -Wl,--gc-sections -Wl,-section-start=.text=0xe000  -mmcu=atmega644p  
	@echo Finished building target: $@
	"d:\WinAVR\bin\avr-objcopy.exe" -O ihex -R .eeprom -R .fuse -R .lock -R .signature -R .user_signatures  "Bootldr.elf" "Bootldr.hex"
	"d:\WinAVR\bin\avr-objcopy.exe" -j .eeprom  --set-section-flags=.eeprom=alloc,load --change-section-lma .eeprom=0  --no-change-warnings -O ihex "Bootldr.elf" "Bootldr.eep" || exit 0
	"d:\WinAVR\bin\avr-objdump.exe" -h -S "Bootldr.elf" > "Bootldr.lss"
	"d:\WinAVR\bin\avr-objcopy.exe" -O srec -R .eeprom -R .fuse -R .lock -R .signature -R .user_signatures "Bootldr.elf" "Bootldr.srec"
	"d:\WinAVR\bin\avr-size.exe" "Bootldr.elf"
	
	





# Other Targets
clean:
	-$(RM) $(OBJS_AS_ARGS) $(EXECUTABLES)  
	-$(RM) $(C_DEPS_AS_ARGS)   
	rm -rf "Bootldr.elf" "Bootldr.a" "Bootldr.hex" "Bootldr.lss" "Bootldr.eep" "Bootldr.map" "Bootldr.srec" "Bootldr.usersignatures"
	