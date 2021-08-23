---
description: El Windows tiene las siguientes acciones estándar.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Referencia de acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e88b4b60e3dd13dc4830a1ea4ba2d16a439546d1ced3dc2a8b7552780548d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627635"
---
# <a name="standard-actions-reference"></a>Referencia de acciones estándar

El Windows tiene las siguientes acciones estándar.



| Nombre de acción                                                     | Breve descripción de la acción                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMINISTRADOR](admin-action.md)                                       | Una acción de nivel superior que se usa para una instalación administrativa.                                                                                                                   |
| [Anunciar](advertise-action.md)                               | Una acción de nivel superior denominada para instalar o quitar componentes anunciados.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Valida que el espacio libre especificado por [**AVAILABLEFREEREG**](availablefreereg.md) existe en el Registro.                                                               |
| [AppSearch](appsearch-action.md)                               | Busca versiones anteriores de productos y determina que las actualizaciones están instaladas.                                                                                        |
| [BindImage](bindimage-action.md)                               | Enlaza archivos ejecutables a archivos DLL importados.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Usa firmas de archivo para validar que los productos aptos están instalados en un sistema antes de realizar una instalación de actualización.                                              |
| [CostFinalize](costfinalize-action.md)                         | Finaliza el proceso de costo de instalación interno iniciado por la [acción CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Inicia el proceso de costo de instalación.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Crea carpetas vacías para los componentes.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Crea accesos directos.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Quita los servicios del sistema.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Deshabilita la reversión para el resto de la instalación.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplica los archivos instalados por la acción InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Comprueba la [**propiedad EXECUTEACTION**](executeaction.md) para determinar qué acción de nivel superior comienza la secuencia de ejecución y, a continuación, ejecuta esa acción.                          |
| [FileCost](filecost-action.md)                                 | Inicializa el cálculo de costos de disco con el instalador. El costo del disco no se finalizará hasta que se ejecute la acción CostFinalize.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Detecta la correspondencia entre la [tabla Actualizar y](upgrade-table.md) los productos instalados.                                                                                 |
| [Forcereboot](forcereboot-action.md)                           | Se usa en la secuencia de acciones para solicitar al usuario un reinicio del sistema durante la instalación.                                                                           |
| [Instalar](install-action.md)                                   | Una acción de nivel superior denominada para instalar o quitar componentes.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copia la base de datos del instalador en el punto de instalación administrativa.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallFinalize. No finaliza la transacción.   |
| [InstallFiles](installfiles-action.md)                         | Copia los archivos del origen al directorio de destino.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Ejecuta un script que contiene todas las operaciones de la secuencia de acciones desde el inicio de la instalación o la última acción InstallFinalize. Marca el final de una transacción. |
| [InstallInitialize](installinitialize-action.md)               | Marca el principio de una transacción.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | La acción InstallSFPCatalogFile instala los catálogos usados por Windows Me para Windows File Protection.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Comprueba que todos los volúmenes con costos con atributos tienen suficiente espacio para la instalación.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Procesa la [tabla IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Evalúa un conjunto de instrucciones condicionales contenidas en la tabla LaunchCondition que deben evaluarse como True antes de que la instalación pueda continuar.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migra los estados de características actuales a la instalación pendiente.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Busca los archivos existentes y los mueve o copia en una nueva ubicación.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configura un servicio para el sistema. **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                           |
| [Acción MsiPublishAssemblies](msipublishassemblies-action.md)  | Administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32 que se están instalando.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Administra el anuncio de ensamblados de Common Language Runtime y ensamblados win32 que se van a quitar.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Instala los controladores ODBC, traductores y orígenes de datos.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Registra un servicio con el sistema.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Consulta la tabla Patch para determinar qué revisiones se aplican a archivos específicos y, a continuación, realiza la aplicación de revisiones por bytes de los archivos.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registra componentes, sus rutas de acceso clave y clientes de componentes.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Anuncia los componentes especificados en la tabla PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Escribe el estado de cada característica en el registro del sistema.                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Publica información del producto con el sistema.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Administra el registro de información de clase COM con el sistema.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | La acción RegisterComPlus registra aplicaciones COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registra información relacionada con la extensión con el sistema.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registra las fuentes instaladas en el sistema.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registra información MIME con el sistema.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registra la información del producto con el instalador y almacena la base de datos del instalador en el equipo local.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registra información de OLE ProgId con el sistema.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registra bibliotecas de tipos con el sistema.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registra la información del usuario para identificar al usuario de un producto.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Elimina los archivos instalados por la acción DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifica los valores de las variables de entorno.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Quita las versiones instaladas de un producto.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Quita los archivos instalados previamente por la acción InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Quita las carpetas vacías vinculadas a los componentes que se va a quitar.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Elimina .ini información de archivo asociada a un componente especificado en la tabla IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Quita orígenes de datos, traductores y controladores ODBC.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Quita las claves del Registro de una aplicación que se crearon de la tabla del Registro.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Determina la ubicación de origen y establece la [**propiedad SourceDir.**](sourcedir.md)                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Usa firmas de archivo para validar que los productos aptos están instalados en un sistema antes de realizar una instalación de actualización.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Solicita al usuario un reinicio del sistema al final de la instalación.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Procesa los módulos de la tabla SelfReg y los registra si están instalados.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Anula el registro de los módulos de la tabla SelfReg que están configurados para desinstalarse.                                                                                                  |
| [Secuencia](sequence-action.md)                                 | Ejecuta las acciones de una tabla especificada por la [**propiedad SEQUENCE.**](sequence.md)                                                                                           |
| [Acción SetODBCFolders](setodbcfolders-action.md)              | Comprueba el sistema para los controladores ODBC existentes y establece el directorio de destino para los nuevos controladores ODBC.                                                                                   |
| [StartServices](startservices-action.md)                       | Inicia los servicios del sistema.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Detiene los servicios del sistema.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Administra la anulación de la inversión de componentes de la tabla PublishComponent y quita información sobre los componentes publicados.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Quita la información de asignación de componentes de características y de estado de selección del registro del sistema.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Administra la eliminación de clases COM del Registro del sistema.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | La acción UnregisterComPlus quita las aplicaciones COM+ del registro.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Administra la eliminación de información relacionada con la extensión del sistema.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Quita la información de registro sobre las fuentes instaladas del sistema.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Anula el registro de información relacionada con MIME del registro del sistema.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Administra la anulación del registro de la información de OLE ProgId con el sistema.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Anula el registro de las bibliotecas de tipos con el sistema.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Establece [**la propiedad ProductID**](productid.md) en el identificador completo del producto.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifica los valores de las variables de entorno.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Escribe .ini de archivo.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Configura la información del Registro.                                                                                                                                                 |



 

 

 




