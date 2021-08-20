---
description: En esta sección se describen las Windows control del registro de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.
title: Funciones de control del Registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7bd7204ada31db6791d3cb78d1a11087d19eae45f0cacbfdf6ae6e032ae66a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676504"
---
# <a name="shell-registry-handling-functions"></a>Funciones de control del Registro de Shell

En esta sección se describen las Windows control del registro de Shell. Los elementos de programación que se explican en esta documentación se exportan Shlwapi.dll y se definen en Shlwapi.h y Shlwapi.lib.

## <a name="in-this-section"></a>En esta sección



| Tema                                                             | Descripción                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Devuelve un puntero a un [**objeto IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations)<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Recupera el tipo percibido de un archivo en función de su extensión.<br/>                                                                                                                |
| [**AssocIsDaous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Determina si un tipo de archivo se considera un riesgo de seguridad potencial.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Busca y recupera una clave relacionada con una asociación de archivos o protocolos del registro.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Busca y recupera una cadena relacionada con la asociación de archivos o protocolos del Registro.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Busca y recupera una cadena relacionada con la asociación de archivos del Registro a partir de una clave especificada.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Copia de forma recursiva las subclaves y los valores de la subclave de origen en la clave de destino. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) no copia los atributos de seguridad de las claves.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Elimina una clave vacía.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Elimina una subclave y todos sus descendientes. Esta función quita la clave y todos los valores de la clave del Registro.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Elimina un valor con nombre de la clave del Registro especificada.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Enumera las subclaves de la clave del Registro abierta especificada.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Enumera los valores de la clave del Registro abierta especificada.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Recupera una matriz de subclaves de clase asociada a un [**objeto IQueryAssociations.**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations)<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Recupera un valor del Registro.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Abre un valor del Registro y proporciona una secuencia que se puede usar para leer o escribir en el valor. Esta función reemplaza a [**SHOpenRegStream.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama)<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Recupera información sobre una clave del Registro especificada.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Abre una clave del Registro y la consulta para un valor específico.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Cierra un identificador a una subclave del Registro específica del usuario en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Crea o abre una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Elimina una subclave del Registro vacía en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Elimina un valor de subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Duplica el identificador HKEY de una clave del Registro.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Enumera las subclaves de una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Enumera los valores de la subclave del Registro especificada en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Recupera un valor booleano de una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Lee un valor de cadena numérico del Registro y lo convierte en un entero.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Recupera una ruta de acceso de archivo del Registro y expande las variables de entorno según sea necesario.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Recupera un valor de una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Abre una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Recupera información sobre una subclave del Registro especificada en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Recupera el tipo y los datos de un nombre especificado asociado a una subclave abierta del Registro en un subárbol específico del usuario (HKEY CURRENT USER o \_ \_ HKEY \_ LOCAL \_ MACHINE).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Toma una ruta de acceso de archivo, reemplaza los nombres de carpeta por cadenas de entorno y coloca la cadena resultante en el Registro.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Establece un valor de subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Establece un valor del Registro.<br/> Use [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) en su lugar.<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Escribe un valor en una subclave del Registro en un subárbol específico del usuario (HKEY \_ CURRENT \_ USER o HKEY LOCAL \_ \_ MACHINE).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Establece el valor de una clave del Registro.<br/>                                                                                                                                        |



 

 

 
