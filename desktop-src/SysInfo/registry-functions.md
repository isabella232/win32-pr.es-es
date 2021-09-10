---
description: Las siguientes son las funciones del Registro.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Funciones del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2cfadd3753b7a269667fee22955f8465495458
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371917"
---
# <a name="registry-functions"></a>Funciones del Registro

Las siguientes son las funciones del Registro.



| Función                                                           | Descripción                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Recupera el tamaño actual del registro y el tamaño máximo que el registro puede alcanzar en el sistema.                          |
| [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Cierra un identificador a la clave del Registro especificada.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Establece una conexión a un identificador del Registro predefinido en otro equipo.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Copia la clave del Registro especificada, junto con sus valores y subclaves, en la clave de destino especificada.                                        |
| [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Crea la clave del Registro especificada.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Crea la clave del Registro especificada y la asocia a una transacción.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Elimina una subclave y sus valores.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Elimina una subclave y sus valores de la vista específica de la plataforma especificada del Registro.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Elimina una subclave y sus valores de la vista específica de la plataforma especificada del Registro como una operación de transacción.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Quita el valor especificado de la clave del Registro y la subclave especificadas.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Elimina las subclaves y los valores de la clave especificada de forma recursiva.                                                                               |
| [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Quita un valor con nombre de la clave del Registro especificada.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Deshabilita el almacenamiento en caché de identificadores para el identificador del Registro predefinido para **HKEY \_ CURRENT \_ USER** para el proceso actual.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Deshabilita el almacenamiento en caché de identificadores para todos los identificadores predefinidos del Registro para el proceso actual.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Deshabilita la reflexión del Registro para la clave especificada.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Habilita la reflexión del Registro para la clave deshabilitada especificada.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Enumera las subclaves de la clave del Registro abierta especificada.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Enumera los valores de la clave del Registro abierta especificada.                                                                                     |
| [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Escribe todos los atributos de la clave del Registro abierta especificada en el Registro.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Recupera una copia del descriptor de seguridad que protege la clave del Registro abierta especificada.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Recupera el tipo y los datos del valor del Registro especificado.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Crea una subclave en **HKEY \_ USERS** o **HKEY \_ LOCAL \_ MACHINE** y almacena la información de registro de un archivo especificado en esa subclave. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Carga la cadena especificada desde la clave y subclave especificadas.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Notifica al autor de la llamada los cambios en los atributos o el contenido de una clave del Registro especificada.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Recupera un identificador de la clave **HKEY \_ CURRENT \_ USER** para el usuario que el subproceso actual está suplantando.                                        |
| [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Abre la clave del Registro especificada.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Abre la clave del Registro especificada y la asocia a una transacción.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Recupera un identificador de la clave **RAÍZ HKEY \_ CLASSES \_** para el usuario especificado.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Mapas una clave del Registro predefinida a una clave del Registro especificada.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Recupera información sobre la clave del Registro especificada.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Recupera el tipo y los datos de una lista de nombres de valor asociados a una clave del Registro abierta.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Determina si la reflexión se ha deshabilitado o habilitado para la clave especificada.                                                              |
| [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Recupera el tipo y los datos de un nombre de valor especificado asociado a una clave del Registro abierta.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Reemplaza el archivo que hace una copia de seguridad de una clave del Registro y todas sus subclaves por otro archivo.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Lee la información del Registro en un archivo especificado y la copia sobre la clave especificada.                                                       |
| [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Guarda la clave especificada y todas sus subclaves y valores en un nuevo archivo.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Guarda la clave especificada y todas sus subclaves y valores en un nuevo archivo. Puede especificar el formato de la clave o el subárbol guardados.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Establece los datos del valor especificado en la clave del Registro y la subclave especificadas.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Establece la seguridad de una clave del Registro abierta.                                                                                                     |
| [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Establece los datos y el tipo de un valor especificado en una clave del Registro.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Descarga la clave del Registro especificada y sus subclaves del Registro.                                                                          |



 

Las siguientes funciones de shell se pueden usar con el Registro:

-   [**AssocCreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**AssocQueryKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**AssocQueryString**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**AssocQueryStringByKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**SHCopyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**SHDeleteEmptyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**SHDeleteKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**SHDeleteValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**SHEnumKeyEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**SHEnumValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**SHGetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**SHQueryInfoKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**SHQueryValueEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**SHRegCloseUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**SHRegCreateUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**SHRegDeleteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**SHRegDuplicateHKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**SHRegEnumUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**SHRegEnumUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**SHRegGetBoolUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**SHRegGetIntW**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**SHRegGetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**SHRegGetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**SHRegOpenUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**SHRegQueryInfoUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**SHRegQueryUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**SHRegSetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**SHRegSetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**SHRegWriteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**SHSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Las siguientes son las funciones de archivo de inicialización. Recuperan información de y copian información en un archivo de inicialización definido por el sistema o por la aplicación. Estas funciones solo se proporcionan para la compatibilidad con versiones de 16 bits de Windows. Las nuevas aplicaciones deben usar el registro.



| Función                                                               | Descripción                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Recupera un entero asociado a una clave en la sección especificada de un archivo de inicialización.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Recupera todas las claves y valores de la sección especificada de un archivo de inicialización.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Recupera los nombres de todas las secciones de un archivo de inicialización.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Recupera una cadena de la sección especificada en un archivo de inicialización.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Recupera los datos asociados a una clave en la sección especificada de un archivo de inicialización.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Recupera un entero de una clave en la sección especificada del Win.ini archivo.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Recupera todas las claves y valores de la sección especificada del Win.ini especificado.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Recupera la cadena asociada a una clave en la sección especificada del Win.ini archivo.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Reemplaza las claves y los valores de la sección especificada en un archivo de inicialización.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Copia una cadena en la sección especificada de un archivo de inicialización.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Copia los datos en una clave de la sección especificada de un archivo de inicialización.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Reemplaza el contenido de la sección especificada en el archivo Win.ini por claves y valores especificados. |
| [**WriteProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Copia una cadena en la sección especificada del Win.ini archivo.                                    |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Estas funciones solo se proporcionan por compatibilidad con versiones de 16 bits de Windows:

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
