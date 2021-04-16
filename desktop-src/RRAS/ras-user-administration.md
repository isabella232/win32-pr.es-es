---
title: Administración de usuarios de RAS
description: Un servidor RAS utiliza una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- RRAS de administración de RAS, administración de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3e357ef813a60c67f991b6e5829879d3e1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676475"
---
# <a name="ras-user-administration"></a>Administración de usuarios de RAS

Un servidor RAS utiliza una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario. La información incluye los privilegios RAS de un usuario, que son un conjunto de marcadores de bits que determinan cómo responde el servidor RAS cuando el usuario llama a para conectarse. Las funciones de administración del servidor RAS localizan la base de datos de cuentas de usuario y obtienen y establecen los privilegios RAS para las cuentas de usuario.

Un servidor RAS puede formar parte de un dominio de sistema operativo o puede ser un equipo independiente que ejecute la versión Server o Professional del sistema operativo. Para un servidor que forma parte de un dominio, la base de datos de cuentas de usuario se almacena en el servidor que es el controlador de dominio principal (PDC). Un servidor independiente almacena su propia base de datos de cuentas de usuario local. Para obtener el nombre del servidor que almacena la base de datos de cuentas de usuario utilizada por un servidor RAS especificado, puede llamar a la función [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) . Después, puede usar el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios en una base de datos de cuentas de usuario. También puede usar el nombre del servidor en las llamadas a las funciones [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) y [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) para obtener y establecer los privilegios ras para una cuenta de usuario especificada.

Las funciones [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) y [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usan la estructura de [**usuario de Ras \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) para especificar los privilegios de Ras y el número de teléfono de devolución de llamada de un usuario. Los privilegios de RAS indican la información siguiente:

-   Si el usuario puede establecer una conexión remota con el servidor o el dominio al que pertenece el servidor.
-   Si el usuario establece una conexión a través de una devolución de llamada, en la que el servidor RAS se cuelga y, a continuación, vuelve a llamar al usuario para establecer la conexión.

Cada cuenta de usuario especifica una de las marcas siguientes para indicar los privilegios de devolución de llamada del usuario.



| Value                      | Significado                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | El servidor RAS no vuelve a llamar al usuario para establecer una conexión.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Cuando el usuario llama a, el servidor RAS se cuelga y llama a un número de teléfono de devolución de llamada preestablecido almacenado en la base de datos de cuentas de usuario. El miembro **szPhoneNumber** de la estructura de [**usuario de Ras \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contiene el número de teléfono de devolución de llamada del usuario.                       |
| RASPRIV \_ CallerSetCallback | Cuando el usuario llama a, el servidor RAS ofrece la opción de especificar un número de teléfono en el que devolver la llamada al usuario. El usuario también puede elegir conectarse inmediatamente sin la devolución de llamada. El miembro **szPhoneNumber** contiene un número predeterminado que el usuario puede invalidar. |



 

 

 