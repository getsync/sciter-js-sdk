# Alternative GNU Make workspace makefile autogenerated by Premake

ifndef config
  config=debug_x32
endif

ifndef verbose
  SILENT = @
endif

ifeq ($(config),debug_x32)
  usciter_config = debug_x32
  sciter_sqlite_config = debug_x32

else ifeq ($(config),debug_x64)
  usciter_config = debug_x64
  sciter_sqlite_config = debug_x64

else ifeq ($(config),debug_arm32)
  usciter_config = debug_arm32
  sciter_sqlite_config = debug_arm32

else ifeq ($(config),debug_arm64)
  usciter_config = debug_arm64
  sciter_sqlite_config = debug_arm64

else ifeq ($(config),release_x32)
  usciter_config = release_x32
  sciter_sqlite_config = release_x32

else ifeq ($(config),release_x64)
  usciter_config = release_x64
  sciter_sqlite_config = release_x64

else ifeq ($(config),release_arm32)
  usciter_config = release_arm32
  sciter_sqlite_config = release_arm32

else ifeq ($(config),release_arm64)
  usciter_config = release_arm64
  sciter_sqlite_config = release_arm64

else
  $(error "invalid configuration $(config)")
endif

PROJECTS := usciter sciter-sqlite

.PHONY: all clean help $(PROJECTS) 

all: $(PROJECTS)

usciter:
ifneq (,$(usciter_config))
	@echo "==== Building usciter ($(usciter_config)) ===="
	@${MAKE} --no-print-directory -C . -f usciter.make config=$(usciter_config)
endif

sciter-sqlite:
ifneq (,$(sciter_sqlite_config))
	@echo "==== Building sciter-sqlite ($(sciter_sqlite_config)) ===="
	@${MAKE} --no-print-directory -C . -f sciter-sqlite.make config=$(sciter_sqlite_config)
endif

clean:
	@${MAKE} --no-print-directory -C . -f usciter.make clean
	@${MAKE} --no-print-directory -C . -f sciter-sqlite.make clean

help:
	@echo "Usage: make [config=name] [target]"
	@echo ""
	@echo "CONFIGURATIONS:"
	@echo "  debug_x32"
	@echo "  debug_x64"
	@echo "  debug_arm32"
	@echo "  debug_arm64"
	@echo "  release_x32"
	@echo "  release_x64"
	@echo "  release_arm32"
	@echo "  release_arm64"
	@echo ""
	@echo "TARGETS:"
	@echo "   all (default)"
	@echo "   clean"
	@echo "   usciter"
	@echo "   sciter-sqlite"
	@echo ""
	@echo "For more information, see https://github.com/premake/premake-core/wiki"