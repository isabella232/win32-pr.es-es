---
title: Derechos de acceso y seguridad de escritorio
description: La seguridad le permite controlar el acceso a los objetos de escritorio. Para obtener más información sobre la seguridad, vea Access-Control Modelo.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805a9b5b3db70bf496d467b774dc7c959030b43d6f89d40aabd0336540b7e56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346695"
---
# <a name="desktop-security-and-access-rights"></a>Derechos de acceso y seguridad de escritorio

La seguridad le permite controlar el acceso a los objetos de escritorio. Para obtener más información sobre la seguridad, vea [Modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model).

Puede especificar un [descriptor de seguridad para](/windows/desktop/SecAuthZ/security-descriptors) un objeto de escritorio al llamar a la función [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) [**o CreateDesktopEx.**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) Si especifica NULL, el escritorio obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para un escritorio proceden de su estación de ventana primaria.

Para obtener o establecer el descriptor de seguridad de un objeto de estación de ventana, llame a las [**funciones GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) [**y SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Al llamar a la [**función OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) o [**OpenInputDesktop,**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto.

Los derechos de acceso válidos para los objetos de escritorio incluyen [los derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) y algunos derechos de acceso específicos del objeto. En la tabla siguiente se enumeran los derechos de acceso estándar utilizados por todos los objetos.

| Valor                       | Significado                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Necesario para eliminar el objeto.                                                                                                                                                                                                                                                       |
| \_CONTROL DE LECTURA (0x00020000L) | Necesario para leer información en el descriptor de seguridad del objeto, sin incluir la información en la SACL. Para leer o escribir la SACL, debe solicitar el derecho de acceso ACCESS \_ SYSTEM \_ SECURITY. Para obtener más información, vea [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right). |
| SYNCHRONIZE (0x00100000L)   | No se admite para objetos de escritorio.                                                                                                                                                                                                                                                   |
| WRITE \_ DAC (0x00040000L)    | Necesario para modificar la DACL en el descriptor de seguridad del objeto .                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Necesario para cambiar el propietario en el descriptor de seguridad del objeto.                                                                                                                                                                                                              |



 

En la tabla siguiente se enumeran los derechos de acceso específicos del objeto.



| Derecho de acceso                       | Descripción                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ CREATEMENU (0x0004L)      | Necesario para crear un menú en el escritorio.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Necesario para crear una ventana en el escritorio.                                                 |
| DESKTOP \_ ENUMERATE (0x0040L)       | Necesario para que se enumere el escritorio.                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)     | Necesario para establecer cualquiera de los enlaces de ventana.                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L) | Necesario para realizar la reproducción de diario en un escritorio.                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)   | Necesario para realizar la grabación de diario en un escritorio.                                         |
| \_READOBJECTS DE ESCRITORIO (0x0001L)     | Necesario para leer objetos en el escritorio.                                                    |
| DESKTOP \_ SWITCHDESKTOP (0x0100L)   | Necesario para activar el escritorio mediante la [**función SwitchDesktop.**](/windows/win32/api/winuser/nf-winuser-switchdesktop) |
| DESKTOP \_ WRITEOBJECTS (0x0080L)    | Necesario para escribir objetos en el escritorio.                                                   |



 

Estos son los derechos [de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un objeto de escritorio contenidos en la estación de ventana interactiva de la sesión de inicio de sesión del usuario.



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
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

Puede solicitar el derecho de acceso ACCESS SYSTEM SECURITY a un objeto de escritorio si desea leer o escribir la \_ \_ SACL del objeto. Para obtener más información, vea [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y Derecho de acceso [sacl](/windows/desktop/SecAuthZ/sacl-access-right).

 

 