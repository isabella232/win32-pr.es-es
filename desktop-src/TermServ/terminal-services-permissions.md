---
title: Servicios de Escritorio remoto permisos
description: Puede usar los permisos proporcionados para Servicios de Escritorio remoto controlar cómo los usuarios y grupos acceden al servidor.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668bf4902ffb133c403e5ea2f74bbc165cf99bca500c95eed5d5dac3cb48a710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999895"
---
# <a name="remote-desktop-services-permissions"></a>Servicios de Escritorio remoto permisos

Puede usar los permisos proporcionados para Servicios de Escritorio remoto controlar cómo los usuarios y grupos acceden al servidor. Para obtener una descripción de los tipos de permisos predeterminados e información más detallada sobre los permisos de Servicios de Escritorio remoto en general, consulte la documentación que acompaña a la herramienta administrativa Servicios de Escritorio remoto Configuration. Para obtener información sobre cómo configurar estos permisos para Windows Server 2008, vea Configurar permisos para Servicios de Escritorio remoto [conexiones](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

A continuación se muestra una lista de los permisos que puede establecer y las tareas que permiten los permisos.



| Value                        | Significado                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consultar información<br/> | Consulte sesiones y servidores para obtener información.<br/>                                                                                                                |
| Establecer información<br/>   | Configure las propiedades de conexión.<br/>                                                                                                                           |
| Control remoto<br/>    | Ver o controlar activamente la sesión de otro usuario.<br/>                                                                                                           |
| Iniciar sesión<br/>             | Inicie sesión en una sesión en el servidor.<br/>                                                                                                                         |
| La opción de cierre de sesión<br/>            | Cierre la sesión de un usuario de una sesión. Tenga en cuenta que cerrar la sesión de un usuario sin advertencia puede provocar la pérdida de datos en el cliente.<br/>                                  |
| Message<br/>           | Envíe un mensaje a las sesiones de otro usuario.<br/>                                                                                                                 |
| Conectar<br/>           | Conectar a otra sesión.<br/>                                                                                                                                |
| Desconectar<br/>        | Desconecte una sesión.<br/>                                                                                                                                      |
| Canales virtuales<br/>  | Use canales virtuales. Tenga en cuenta que al desactivar los canales virtuales se deshabilitan algunas Servicios de Escritorio remoto como el Portapapeles y el redireccionamiento de impresoras.<br/> |
| Reset<br/>             | Finalizar una sesión. Tenga en cuenta que finalizar una sesión sin advertencia puede provocar la pérdida de datos en el cliente.<br/>                                                    |



 

El permiso Logon es necesario para que un usuario inicie sesión en una nueva Servicios de Escritorio remoto sesión. Todos los demás Servicios de Escritorio remoto permisos se aplican al control de la sesión de Servicios de Escritorio remoto usuario.

Servicios de Escritorio remoto se pueden conceder o establecer permisos para usuarios o grupos individuales. Los usuarios también pueden heredar permisos como resultado de ser miembros de un grupo. Sin embargo, la denegación de un permiso invalida un permiso heredado. Por ejemplo, a los miembros del grupo Escritorio remoto usuarios (RDU) se les concede el permiso Consulta de forma predeterminada. Si un administrador establece el permiso Consulta en "Denegar" para ese usuario, el usuario no podrá consultar la sesión de otro usuario. Una vez que un usuario inicia sesión en una sesión, se le conceden todos los demás Servicios de Escritorio remoto permisos para su sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios de Escritorio remoto de administración de aplicaciones](terminal-services-management-applications.md)
</dt> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

