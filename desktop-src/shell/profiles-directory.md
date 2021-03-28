---
description: 'El sistema almacena información de Perfil de usuario en un directorio específico, que tiene nombres diferentes en versiones diferentes de Windows: &\# 0034; Documents and settings&\# 0034; en Windows XP y &\# 0034; Usuarios&\# 0034; en Windows Vista y versiones posteriores.'
title: Directorio de perfiles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985635"
---
# <a name="profiles-directory"></a>Directorio de perfiles

El sistema almacena información de Perfil de usuario en un directorio específico, que tiene nombres diferentes en versiones diferentes de Windows: "Documents and Settings" en Windows XP y "Users" en Windows Vista y versiones posteriores. Para obtener la ruta de acceso del directorio de perfiles, utilice la función [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .

El directorio de perfiles contiene los siguientes subdirectorios para los perfiles de usuario.



| Directorio                                      | Descripción                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista o posterior)/all usuarios | Información del programa que se aplica a todos los usuarios. El directorio todos los usuarios sigue existiendo en Windows Vista o posterior, por compatibilidad con versiones anteriores. |
| Valor predeterminado                                        | Información de perfil que se aplica al usuario predeterminado.                                                                                      |
| *User*                                         | Información de perfil que se aplica al usuario especificado. Cada usuario tiene su propio subdirectorio de perfil.                                      |



 

Para obtener la ubicación del directorio ProgramData/All Users, llame a la función [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) . Este directorio raíz contiene los siguientes subdirectorios:



| Directorio  | Descripción                          |
|------------|--------------------------------------|
| Escritorio    | Accesos directos que se van a mostrar en el escritorio. |
| Menú Inicio | Elementos de menú para el menú **Inicio** .   |



 

Para obtener la ubicación del directorio del usuario predeterminado, llame a la función [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) . Para obtener la ubicación del directorio de un usuario determinado, llame a la función [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) . El usuario predeterminado y los directorios de usuario específicos contienen los siguientes subdirectorios. Los directorios en cursiva indican directorios que están ocultos de forma predeterminada. Puede ver estos directorios seleccionando la opción **Mostrar archivos, carpetas y unidades ocultos** en el elemento del panel de control **Opciones de carpeta** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Directorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datos de aplicaciones</td>
<td>Datos específicos de la aplicación.</td>
</tr>
<tr class="even">
<td>Cookies</td>
<td>Cookies de Windows Internet Explorer.</td>
</tr>
<tr class="odd">
<td>Escritorio</td>
<td>Accesos directos que se van a mostrar en el escritorio.</td>
</tr>
<tr class="even">
<td>Favoritos</td>
<td>Vínculos a sitios web favoritos.</td>
</tr>
<tr class="odd">
<td>Configuración local</td>
<td>La configuración de la aplicación y los datos que no se mueven con el perfil. Normalmente, la configuración o los datos de este directorio son específicos del equipo, o bien son demasiado grandes para moverse de forma eficaz. Este directorio contiene las siguientes subcarpetas:
<ul>
<li>Datos de aplicaciones</li>
<li>Historial</li>
<li>Temp</li>
<li>Archivos temporales de Internet</li>
</ul></td>
</tr>
<tr class="even">
<td>Mis documentos</td>
<td>La ubicación predeterminada de los documentos que el usuario crea. De forma predeterminada, las aplicaciones deben guardar los archivos de documento en este directorio.</td>
</tr>
<tr class="odd">
<td><em>NetHood</em></td>
<td>Accesos directos a elementos de entorno de red.</td>
</tr>
<tr class="even">
<td><em>PrintHood</em></td>
<td>Accesos directos a elementos de carpeta de impresora.</td>
</tr>
<tr class="odd">
<td><em>Recientes</em></td>
<td>Accesos directos a los documentos usados más recientemente.</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>Accesos directos a ubicaciones a las que el usuario suele enviar archivos.</td>
</tr>
<tr class="odd">
<td>Menú Inicio</td>
<td>Elementos de menú para el menú <strong>Inicio</strong> .</td>
</tr>
<tr class="even">
<td><em>Templates</em> (Plantillas [C++])</td>
<td>Accesos directos a elementos de plantilla.</td>
</tr>
</tbody>
</table>



 

Para obtener la ubicación de los subdirectorios de estos directorios, use las funciones [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) o [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

 

 



