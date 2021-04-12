---
title: Servicios de Escritorio remoto permisos
description: Puede usar los permisos proporcionados para Servicios de Escritorio remoto para controlar el modo en que los usuarios y los grupos acceden al servidor.
ms.assetid: 448a7f9b-bf12-48eb-a3e7-4512ec288d95
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1358a4360889bc013beefcee4e029f3572c9c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420831"
---
# <a name="remote-desktop-services-permissions"></a>Servicios de Escritorio remoto permisos

Puede usar los permisos proporcionados para Servicios de Escritorio remoto para controlar el modo en que los usuarios y los grupos acceden al servidor. Para obtener una descripción de los tipos de permisos predeterminados e información más detallada sobre los permisos de Servicios de Escritorio remoto en general, consulte la documentación que acompaña a la herramienta administrativa de configuración de Servicios de Escritorio remoto. Para obtener información sobre la configuración de estos permisos para Windows Server 2008, vea [configurar permisos para conexiones servicios de escritorio remoto](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753032(v=ws.11)).

A continuación se muestra una lista de los permisos que puede establecer y las tareas que los permisos permiten.



| Value                        | Significado                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consultar información<br/> | Consulte las sesiones y los servidores para obtener información.<br/>                                                                                                                |
| Establecer información<br/>   | Configurar las propiedades de la conexión.<br/>                                                                                                                           |
| Control remoto<br/>    | Ver o controlar activamente la sesión de otro usuario.<br/>                                                                                                           |
| Iniciar sesión<br/>             | Inicie sesión en una sesión de en el servidor.<br/>                                                                                                                         |
| La opción de cierre de sesión<br/>            | Cerrar sesión de un usuario. Tenga en cuenta que el cierre de sesión de un usuario sin advertencia puede provocar la pérdida de datos en el cliente.<br/>                                  |
| Message<br/>           | Envía un mensaje a las sesiones de otro usuario.<br/>                                                                                                                 |
| Conectar<br/>           | Conéctese a otra sesión.<br/>                                                                                                                                |
| Desconectar<br/>        | Desconectar una sesión.<br/>                                                                                                                                      |
| Canales virtuales<br/>  | Usar canales virtuales. Tenga en cuenta que la desactivación de los canales virtuales deshabilita algunas características de Servicios de Escritorio remoto, como el portapapeles y la redirección de la impresora.<br/> |
| Reset<br/>             | Finalizar una sesión. Tenga en cuenta que el final de una sesión sin advertencia puede producir la pérdida de datos en el cliente.<br/>                                                    |



 

El permiso de inicio de sesión es necesario para que un usuario inicie sesión en una nueva sesión de Servicios de Escritorio remoto. El resto de los permisos de Servicios de Escritorio remoto se aplican al control de la sesión Servicios de Escritorio remoto de otro usuario.

Se pueden conceder o establecer Servicios de Escritorio remoto permisos para usuarios individuales o grupos. Los usuarios también pueden heredar permisos como resultado de ser miembros del grupo. Sin embargo, la denegación de un permiso invalida un permiso heredado. Por ejemplo, de forma predeterminada, se concede el permiso de consulta a los miembros del grupo Escritorio remoto usuarios (RDU). Si un administrador establece el permiso de consulta en "denegar" para ese usuario, el usuario no podrá consultar la sesión de otro usuario. Después de que un usuario inicie sesión en una sesión, se concede al usuario todos los demás Servicios de Escritorio remoto permisos para su sesión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de administración de Servicios de Escritorio remoto](terminal-services-management-applications.md)
</dt> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

