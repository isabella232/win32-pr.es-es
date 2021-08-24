---
title: Administración de usuarios ras
description: Un servidor RAS usa una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- RAS Administration RRAS , user administration (RRAS de administración de RAS), administración de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e4916a9cf6138ebb6c201e9301feacbe332649036e7eb18075df621512a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028645"
---
# <a name="ras-user-administration"></a>Administración de usuarios ras

Un servidor RAS usa una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario. La información incluye los privilegios RAS de un usuario, que son un conjunto de marcas de bits que determinan cómo responde el servidor RAS cuando el usuario llama a para conectarse. Las funciones de administración del servidor RAS localizan la base de datos de la cuenta de usuario y obtienen y establecen los privilegios ras para las cuentas de usuario.

Un servidor RAS puede formar parte de un dominio de sistema operativo o puede ser una máquina independiente que ejecute el servidor o la versión profesional del sistema operativo. Para un servidor que forma parte de un dominio, la base de datos de la cuenta de usuario se almacena en el servidor que es el controlador de dominio principal (PDC). Un servidor independiente almacena su propia base de datos de cuentas de usuario local. Para obtener el nombre del servidor que almacena la base de datos de cuentas de usuario utilizada por un servidor RAS especificado, puede llamar a la función [**MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) A continuación, puede usar el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios de una base de datos de cuentas de usuario. También puede usar el nombre del servidor en las llamadas a las funciones [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) y [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) para obtener y establecer los privilegios RAS para una cuenta de usuario especificada.

Las [**funciones MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) y [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usan la estructura [**RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) para especificar los privilegios RAS de un usuario y el número de teléfono de de vuelta. Los privilegios ras indican la siguiente información:

-   Si el usuario puede realizar una conexión remota al servidor o al dominio al que pertenece el servidor.
-   Si el usuario establece una conexión a través de una llamada de vuelta, en la que el servidor RAS se para y, a continuación, vuelve a llamar al usuario para establecer la conexión.

Cada cuenta de usuario especifica una de las marcas siguientes para indicar los privilegios de desuso del usuario.



| Value                      | Significado                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | El servidor RAS no llama al usuario para establecer una conexión.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Cuando el usuario llama a , el servidor RAS se para y llama a un número de teléfono preestablecido almacenado en la base de datos de la cuenta de usuario. El **miembro szPhoneNumber** de la [**estructura RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contiene el número de teléfono de llamada del usuario.                       |
| RASPRIV \_ CallerSetCallback | Cuando el usuario llama a , el servidor RAS proporciona la opción de especificar un número de teléfono en el que llamar al usuario. El usuario también puede optar por conectarse inmediatamente sin la de vuelta. El **miembro szPhoneNumber** contiene un número predeterminado que el usuario puede invalidar. |



 

 

 