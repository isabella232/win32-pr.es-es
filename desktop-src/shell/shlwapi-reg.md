---
description: En esta sección se describen las funciones de control del registro del shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.
title: Funciones de control del registro de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8a3e4f65904fa97635b3ef4dc3abd9f01344f6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997901"
---
# <a name="shell-registry-handling-functions"></a>Funciones de control del registro de Shell

En esta sección se describen las funciones de control del registro del shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.

## <a name="in-this-section"></a>En esta sección



| Tema                                                             | Descripción                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Devuelve un puntero a un objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Recupera el tipo percibido de un archivo en función de su extensión.<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Determina si un tipo de archivo se considera un riesgo de seguridad potencial.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Busca y recupera una clave relacionada con un archivo o una asociación de protocolo del registro.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Busca y recupera una cadena relacionada con la Asociación de archivos o protocolos del registro.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Busca y recupera una cadena relacionada con la Asociación de archivos desde el registro a partir de una clave especificada.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Copia de forma recursiva las subclaves y los valores de la subclave de origen en la clave de destino. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) no copia los atributos de seguridad de las claves.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Elimina una clave vacía.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Elimina una subclave y todos sus descendientes. Esta función quita la clave y todos los valores de la clave del registro.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Elimina un valor con nombre de la clave del registro especificada.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Enumera las subclaves de la clave del registro abierta especificada.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Enumera los valores de la clave del registro abierta especificada.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Recupera una matriz de subclaves de clase asociada a un objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Recupera un valor del registro.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Abre un valor del registro y proporciona una secuencia que se puede utilizar para leer o escribir en el valor. Esta función reemplaza a [**SHOpenRegStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama).<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Recupera información sobre una clave del registro especificada.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Abre una clave del registro y la consulta para obtener un valor específico.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Cierra un identificador a una subclave del registro específica del usuario en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Crea o abre una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Elimina una subclave del Registro vacía en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Elimina un valor de subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Duplica el identificador HKEY de una clave del registro.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Enumera las subclaves de una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Enumera los valores de la subclave del registro especificada en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Recupera un valor booleano de una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Lee un valor de cadena numérico del registro y lo convierte en un entero.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Recupera una ruta de acceso de archivo del registro y expande las variables de entorno según sea necesario.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Recupera un valor de una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Abre una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Recupera información sobre una subclave del registro especificada en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Recupera el tipo y los datos para un nombre especificado asociado a una subclave del registro abierta en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Toma una ruta de acceso de archivo, reemplaza los nombres de carpeta por cadenas de entorno y coloca la cadena resultante en el registro.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Establece un valor de subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Establece un valor del registro.<br/> Use [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) en su lugar.<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Escribe un valor en una subclave del registro en un subárbol específico del usuario (HKEY \_ Current \_ User o HKEY \_ local \_ Machine).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Establece el valor de una clave del registro.<br/>                                                                                                                                        |



 

 

 
