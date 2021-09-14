---
description: 'El sistema almacena información de perfil de usuario en un directorio específico, que tiene nombres diferentes en distintas versiones de Windows: &\# 0034;Documents y Configuración&\# 0034; en Windows XP y &\# 0034; Los&\# 0034; en Windows Vista y versiones posteriores.'
title: Directorio de perfiles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40e9f795c800a3a688f3b032db53cba755849db6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256934"
---
# <a name="profiles-directory"></a>Directorio de perfiles

El sistema almacena la información de perfil de usuario en un directorio específico, que tiene nombres diferentes en diferentes versiones de Windows: "Documentos y Configuración" en Windows XP y "Usuarios" en Windows Vista y versiones posteriores. Para obtener la ruta de acceso del directorio profiles, use la [**función GetProfilesDirectory.**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)

El directorio profiles contiene los siguientes subdirectorios para perfiles de usuario.



| Directorio                                      | Descripción                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista o posterior)/Todos los usuarios | Información del programa que se aplica a todos los usuarios. El directorio Todos los usuarios sigue existiendo en Windows Vista o versiones posteriores, por compatibilidad con versiones anteriores. |
| Valor predeterminado                                        | Información de perfil que se aplica al usuario predeterminado.                                                                                      |
| *User*                                         | Información de perfil que se aplica al usuario especificado. Cada usuario tiene su propio subdirectorio de perfil.                                      |



 

Para obtener la ubicación del directorio ProgramData/All Users, llame a la [**función GetAllUsersProfileDirectory.**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) Este directorio raíz contiene los siguientes subdirectorios:



| Directorio  | Descripción                          |
|------------|--------------------------------------|
| Escritorio    | Accesos directos que se mostrarán en el escritorio. |
| Menú Inicio | Elementos de menú del **menú** Inicio.   |



 

Para obtener la ubicación del directorio del usuario predeterminado, llame a la [**función GetDefaultUserProfileDirectory.**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) Para obtener la ubicación del directorio de un usuario determinado, llame a la [**función GetUserProfileDirectory.**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) Tanto el usuario predeterminado como los directorios de usuario específicos contienen los siguientes subdirectorios. Los directorios en cursiva indican directorios que están ocultos de forma predeterminada. Puede ver estos directorios seleccionando la opción Mostrar **archivos,** carpetas y unidades ocultos en el elemento del panel de **control** Opciones de carpeta.




| Directorio | Descripción | 
|-----------|-------------|
| Datos de aplicaciones | Datos específicos de la aplicación. | 
| Cookies | Windows Internet Explorer cookies. | 
| Escritorio | Accesos directos que se mostrarán en el escritorio. | 
| Favoritos | Vínculos a sitios web favoritos. | 
| Configuración Configuración | Configuración de la aplicación y datos que no se recorren con el perfil. Normalmente, la configuración o los datos de este directorio son específicos del equipo o son demasiado grandes para recorrer de forma eficaz. Este directorio contiene las subcarpetas siguientes:<ul><li>Datos de aplicaciones</li><li>Historial</li><li>Temp</li><li>Archivos temporales de Internet</li></ul> | 
| Mis documentos | Ubicación predeterminada de los documentos que crea el usuario. Las aplicaciones deben guardar los archivos de documento en este directorio de forma predeterminada. | 
| <em>Net Establa</em> | Accesos directos a elementos del entorno de red. | 
| <em>Print (Imprimir)Print (Imprimir)</em> | Accesos directos a elementos de carpeta de impresora. | 
| <em>Recientes</em> | Accesos directos a los documentos usados más recientemente. | 
| Sendto | Accesos directos a ubicaciones a las que el usuario suele enviar archivos. | 
| Menú Inicio | Elementos de menú del <strong>menú</strong> Inicio. | 
| <em>Templates</em> (Plantillas [C++]) | Accesos directos a elementos de plantilla. | 




 

Para obtener la ubicación de los subdirectorios de estos directorios, use las funciones [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) o [**SHGetKnownFolderPath.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)

 

 



