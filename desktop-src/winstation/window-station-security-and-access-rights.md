---
title: Seguridad y derechos de acceso de la estación de ventana
description: La seguridad le permite controlar el acceso a los objetos de la estación de ventana. Para obtener más información sobre la seguridad, vea modelo de Access-Control.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714385"
---
# <a name="window-station-security-and-access-rights"></a>Seguridad y derechos de acceso de la estación de ventana

La seguridad le permite controlar el acceso a los objetos de la estación de ventana. Para obtener más información sobre la seguridad, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors) para un objeto de estación de ventana cuando llame a la función [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) . Si especifica NULL, la estación de ventana obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado de una estación de ventana proceden del token principal o de suplantación del creador.

Para obtener o establecer el descriptor de seguridad de un objeto de estación de ventana, llame a las funciones [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Cuando se llama a la función [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.

Los derechos de acceso válidos para los objetos de la estación de ventana incluyen los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) y algunos derechos de acceso específicos del objeto. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Value                       | Significado                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELIMINAR (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                       |
| CONTROL de lectura \_ (0x00020000L) | Necesario para leer la información del descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ . Para obtener más información, consulte [derechos de acceso de SACL](/windows/desktop/SecAuthZ/sacl-access-right). |
| SINCRONIZAr (0x00100000L)   | No se admite para objetos de estación de ventana.                                                                                                                                                                                                                                            |
| ESCRIBIR \_ DAC (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad para el objeto.                                                                                                                                                                                                               |
| Propietario de escritura \_ (0x00080000L)  | Necesario para cambiar el propietario del descriptor de seguridad para el objeto.                                                                                                                                                                                                              |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto.



| Derecho de acceso                        | Descripción                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ todos los \_ accesos (0x37F)         | Todos los derechos de acceso posibles para la estación de ventana.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Necesario para usar el portapapeles.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Necesario para manipular átomos globales.                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)     | Se requiere para crear nuevos objetos de escritorio en la estación de ventana.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Necesario para enumerar los objetos de escritorio existentes.                                                                                                                                                                                                                               |
| \_Enumeración de WINSTA (0x0100L)         | Necesario para que se Enumere la estación de ventana.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Necesario para llamar correctamente a la función [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) . Los usuarios pueden compartir las estaciones de ventana y este tipo de acceso puede impedir que otros usuarios de una estación de ventana cierren la sesión del propietario de la estación de ventana. |
| WINSTA \_ READATTRIBUTES (0x0002L)    | Necesario para leer los atributos de un objeto de estación de ventana. Este atributo incluye la configuración de color y otras propiedades de la estación de ventana global.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Necesario para tener acceso al contenido de la pantalla.                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)   | Necesario para modificar los atributos de un objeto de estación de ventana. Los atributos incluyen la configuración de color y otras propiedades de la estación de ventana global.                                                                                                                               |



 

A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para el objeto de estación de ventana interactiva, que es la estación de ventana asignada a la sesión de inicio de sesión del usuario interactivo.



<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un objeto de estación de ventana no interactiva. El sistema asigna estaciones de ventana no interactivas a todas las sesiones de inicio de sesión distintas de las del usuario interactivo.



<table>
<thead>
<tr class="header">
<th>Derecho de acceso</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Puede solicitar el derecho de \_ acceso de seguridad del sistema de acceso \_ a un objeto de estación de ventana si desea leer o escribir la SACL del objeto. Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [SACL](/windows/desktop/SecAuthZ/sacl-access-right).

 

 