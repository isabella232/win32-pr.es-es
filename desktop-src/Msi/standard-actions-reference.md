---
description: El Windows Installer tiene las siguientes acciones estándar.
ms.assetid: 219b5eb6-501f-4e30-b398-4ed5e0cdf2ab
title: Referencia de acciones estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5104c39639ff2bc7b504996467cf707eb52bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276369"
---
# <a name="standard-actions-reference"></a>Referencia de acciones estándar

El Windows Installer tiene las siguientes acciones estándar.



| Nombre de acción                                                     | Breve descripción de la acción                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ADMINISTRADOR](admin-action.md)                                       | Una acción de nivel superior que se usa para una instalación administrativa.                                                                                                                   |
| [ANUNCIA](advertise-action.md)                               | Una acción de nivel superior llamada para instalar o quitar componentes anunciados.                                                                                                         |
| [AllocateRegistrySpace](allocateregistryspace-action.md)       | Valida que el espacio disponible especificado por [**AVAILABLEFREEREG**](availablefreereg.md) existe en el registro.                                                               |
| [AppSearch](appsearch-action.md)                               | Busca versiones anteriores de los productos y determina que se instalan las actualizaciones.                                                                                        |
| [BindImage](bindimage-action.md)                               | Enlaza los ejecutables a los archivos dll importados.                                                                                                                                           |
| [CCPSearch](ccpsearch-action.md)                               | Usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.                                              |
| [CostFinalize](costfinalize-action.md)                         | Finaliza el proceso de costo de instalación interna Iniciado por la [acción CostInitialize](costinitialize-action.md).                                                               |
| [CostInitialize](costinitialize-action.md)                     | Inicia el proceso de costo de instalación.                                                                                                                                      |
| [CreateFolders](createfolders-action.md)                       | Crea carpetas vacías para los componentes de.                                                                                                                                         |
| [CreateShortcuts](createshortcuts-action.md)                   | Crea accesos directos.                                                                                                                                                            |
| [DeleteServices](deleteservices-action.md)                     | Quita los servicios del sistema.                                                                                                                                                      |
| [DisableRollback](disablerollback-action.md)                   | Deshabilita la reversión para el resto de la instalación.                                                                                                                      |
| [DuplicateFiles](duplicatefiles-action.md)                     | Duplica los archivos instalados por la acción InstallFiles.                                                                                                                        |
| [ExecuteAction](executeaction-action.md)                       | Comprueba la propiedad [**EXECUTEACTION**](executeaction.md) para determinar qué acción de nivel superior comienza la secuencia de ejecución y, a continuación, ejecuta esa acción.                          |
| [FileCost](filecost-action.md)                                 | Inicializa el cálculo del costo del disco con el instalador. El coste de los discos no se finaliza hasta que se ejecuta la acción CostFinalize.                                                |
| [FindRelatedProducts](findrelatedproducts-action.md)           | Detecta la correspondencia entre la [tabla de actualización](upgrade-table.md) y los productos instalados.                                                                                 |
| [ForceReboot](forcereboot-action.md)                           | Se usa en la secuencia de acciones para solicitar al usuario que se reinicie el sistema durante la instalación.                                                                           |
| [INSTALADOS](install-action.md)                                   | Una acción de nivel superior llamada para instalar o quitar componentes.                                                                                                                    |
| [InstallAdminPackage](installadminpackage-action.md)           | Copia la base de datos del instalador en el punto de instalación administrativa.                                                                                                       |
| [InstallExecute](installexecute-action.md)                     | Ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción de InstallFinalize. No finaliza la transacción.   |
| [InstallFiles](installfiles-action.md)                         | Copia los archivos del directorio de origen al de destino.                                                                                                                    |
| [InstallFinalize](installfinalize-action.md)                   | Ejecuta un script que contiene todas las operaciones de la secuencia de acción desde el inicio de la instalación o la última acción de InstallFinalize. Marca el final de una transacción. |
| [InstallInitialize](installinitialize-action.md)               | Marca el inicio de una transacción.                                                                                                                                         |
| [InstallSFPCatalogFile](installsfpcatalogfile-action.md)       | La acción InstallSFPCatalogFile instala los catálogos que usa Windows me para la protección de archivos de Windows.                                                                        |
| [InstallValidate](installvalidate-action.md)                   | Comprueba que todos los volúmenes con costos atribuidos tienen suficiente espacio para la instalación.                                                                                   |
| [IsolateComponents](isolatecomponents-action.md)               | Procesa la [tabla IsolatedComponent](isolatedcomponent-table.md)                                                                                                          |
| [LaunchConditions](launchconditions-action.md)                 | Evalúa un conjunto de instrucciones condicionales contenidas en la tabla LaunchCondition que deben evaluarse como true antes de que pueda continuar la instalación.                          |
| [MigrateFeatureStates](migratefeaturestates-action.md)         | Migra los Estados de características actuales a la instalación pendiente.                                                                                                                  |
| [MoveFiles](movefiles-action.md)                               | Busca los archivos existentes y mueve o copia esos archivos en una nueva ubicación.                                                                                                     |
| [MsiConfigureServices](msiconfigureservices-action.md)         | Configura un servicio para el sistema. **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                           |
| [Acción MsiPublishAssemblies](msipublishassemblies-action.md)  | Administra el anuncio de Common Language Runtime ensamblados y ensamblados Win32 que se están instalando.                                                                |
| [MsiUnpublishAssemblies](msiunpublishassemblies-action.md)     | Administra el anuncio de Common Language Runtime ensamblados y ensamblados Win32 que se van a quitar.                                                                  |
| [InstallODBC](installodbc-action.md)                           | Instala los controladores, traductores y orígenes de datos ODBC.                                                                                                                     |
| [InstallServices](installservices-action.md)                   | Registra un servicio con el sistema.                                                                                                                                          |
| [PatchFiles](patchfiles-action.md)                             | Consulta la tabla patch para determinar qué revisiones se aplican a determinados archivos y, a continuación, realiza la aplicación de revisiones en bytes de los archivos.                                       |
| [ProcessComponents](processcomponents-action.md)               | Registra los componentes, sus rutas de acceso clave y los clientes de componentes.                                                                                                                 |
| [PublishComponents](publishcomponents-action.md)               | Anuncia los componentes especificados en la tabla PublishComponent.                                                                                                            |
| [PublishFeatures](publishfeatures-action.md)                   | Escribe el estado de la característica de cada característica en el registro del sistema.                                                                                                             |
| [PublishProduct](publishproduct-action.md)                     | Publica información del producto con el sistema.                                                                                                                                |
| [RegisterClassInfo](registerclassinfo-action.md)               | Administra el registro de información de clase COM con el sistema.                                                                                                            |
| [RegisterComPlus](registercomplus-action.md)                   | La acción RegisterComPlus registra las aplicaciones COM+.                                                                                                                       |
| [RegisterExtensionInfo](registerextensioninfo-action.md)       | Registra información relacionada con la extensión con el sistema.                                                                                                                      |
| [RegisterFonts](registerfonts-action.md)                       | Registra las fuentes instaladas en el sistema.                                                                                                                                    |
| [RegisterMIMEInfo](registermimeinfo-action.md)                 | Registra información de MIME con el sistema.                                                                                                                                   |
| [RegisterProduct](registerproduct-action.md)                   | Registra información del producto con el instalador y almacena la base de datos del instalador en el equipo local.                                                                     |
| [RegisterProgIdInfo](registerprogidinfo-action.md)             | Registra información de OLE ProgId en el sistema.                                                                                                                             |
| [RegisterTypeLibraries](registertypelibraries-action.md)       | Registra las bibliotecas de tipos con el sistema.                                                                                                                                     |
| [RegisterUser](registeruser-action.md)                         | Registra información de usuario para identificar al usuario de un producto.                                                                                                                 |
| [RemoveDuplicateFiles](removeduplicatefiles-action.md)         | Elimina los archivos instalados por la acción DuplicateFiles.                                                                                                                         |
| [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) | Modifica los valores de las variables de entorno.                                                                                                                                 |
| [RemoveExistingProducts](removeexistingproducts-action.md)     | Quita las versiones instaladas de un producto.                                                                                                                                      |
| [RemoveFiles](removefiles-action.md)                           | Quita los archivos instalados previamente por la acción InstallFiles.                                                                                                                |
| [RemoveFolders](removefolders-action.md)                       | Quita las carpetas vacías vinculadas a los componentes que se van a quitar.                                                                                                                 |
| [RemoveIniValues](removeinivalues-action.md)                   | Elimina la información del archivo. ini asociada a un componente especificado en la tabla IniFile.                                                                                     |
| [RemoveODBC](removeodbc-action.md)                             | Quita los orígenes de datos, los traductores y los controladores ODBC.                                                                                                                          |
| [RemoveRegistryValues](removeregistryvalues-action.md)         | Quita las claves del registro de una aplicación que se crearon a partir de la tabla del registro.                                                                                            |
| [RemoveShortcuts](removeshortcuts-action.md)                   | Administra la eliminación de un acceso directo anunciado cuya característica está seleccionada para la desinstalación.                                                                                   |
| [ResolveSource](resolvesource-action.md)                       | Determina la ubicación de origen y establece la propiedad [**SourceDir**](sourcedir.md) .                                                                                          |
| [RMCCPSearch](rmccpsearch-action.md)                           | Usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.                                              |
| [ScheduleReboot](schedulereboot-action.md)                     | Solicita al usuario que se reinicie el sistema al final de la instalación.                                                                                                         |
| [SelfRegModules](selfregmodules-action.md)                     | Procesa módulos en la tabla SelfReg y los registra si están instalados.                                                                                              |
| [SelfUnregModules](selfunregmodules-action.md)                 | Anula el registro de los módulos de la tabla SelfReg que están configurados para desinstalarse.                                                                                                  |
| [SEQUENCE](sequence-action.md)                                 | Ejecuta las acciones en una tabla especificada por la propiedad [**Sequence**](sequence.md) .                                                                                           |
| [Acción SetODBCFolders](setodbcfolders-action.md)              | Comprueba si hay controladores ODBC existentes en el sistema y establece el directorio de destino para los nuevos controladores ODBC.                                                                                   |
| [StartServices](startservices-action.md)                       | Inicia servicios del sistema.                                                                                                                                                       |
| [StopServices](stopservices-action.md)                         | Detiene los servicios del sistema.                                                                                                                                                        |
| [UnpublishComponents](unpublishcomponents-action.md)           | Administra el desanuncio de los componentes de la tabla PublishComponent y quita la información sobre los componentes publicados.                                                 |
| [UnpublishFeatures](unpublishfeatures-action.md)               | Quita la información de asignación del componente de la selección y el estado del registro del sistema.                                                                               |
| [UnregisterClassInfo](unregisterclassinfo-action.md)           | Administra la eliminación de clases COM del registro del sistema.                                                                                                                  |
| [UnregisterComPlus](unregistercomplus-action.md)               | La acción UnregisterComPlus quita las aplicaciones COM+ del registro.                                                                                                     |
| [UnregisterExtensionInfo](unregisterextensioninfo-action.md)   | Administra la eliminación de la información relacionada con la extensión del sistema.                                                                                                         |
| [UnregisterFonts](unregisterfonts-action.md)                   | Quita del sistema la información de registro sobre las fuentes instaladas.                                                                                                       |
| [UnregisterMIMEInfo](unregistermimeinfo-action.md)             | Anula el registro de la información relacionada con MIME del registro del sistema.                                                                                                                |
| [UnregisterProgIdInfo](unregisterprogidinfo-action.md)         | Administra la anulación del registro de información de identificador de programa OLE con el sistema.                                                                                                         |
| [UnregisterTypeLibraries](unregistertypelibraries-action.md)   | Anula el registro de bibliotecas de tipos con el sistema.                                                                                                                                   |
| [ValidateProductID](validateproductid-action.md)               | Establece la propiedad [**ProductID**](productid.md) en el identificador de producto completo.                                                                                                  |
| [WriteEnvironmentStrings](writeenvironmentstrings-action.md)   | Modifica los valores de las variables de entorno.                                                                                                                                 |
| [WriteIniValues](writeinivalues-action.md)                     | Escribe la información del archivo. ini.                                                                                                                                                 |
| [WriteRegistryValues](writeregistryvalues-action.md)           | Configura la información del registro.                                                                                                                                                 |



 

 

 




