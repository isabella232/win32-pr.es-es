---
title: Administración de cuentas de usuario RAS
description: Un servidor RAS de Windows NT 4,0 utiliza una base de datos de cuentas de usuario que contiene información acerca de un conjunto de cuentas de usuario.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d090fc16e7d731525b79493119f3c604e043c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359056"
---
# <a name="ras-user-account-administration"></a>Administración de cuentas de usuario RAS

Un servidor RAS de Windows NT 4,0 utiliza una base de datos de cuentas de usuario que contiene información acerca de un conjunto de cuentas de usuario. La información incluye los privilegios RAS de un usuario, que son un conjunto de marcadores de bits que determinan cómo responde el servidor RAS cuando el usuario llama a para conectarse. Las funciones de administración del servidor RAS permiten localizar la base de datos de cuentas de usuario y obtener y establecer los privilegios RAS para las cuentas de usuario.

Un servidor RAS de Windows NT 4,0 puede formar parte de un dominio de Windows NT/Windows 2000, o bien puede ser un servidor o una estación de trabajo de Windows NT independiente que no forme parte de un dominio. Para un servidor que forma parte de un dominio, la base de datos de cuentas de usuario se almacena en el servidor que es el controlador de dominio principal (PDC). Un servidor independiente almacena su propia base de datos de cuentas de usuario local. Para obtener el nombre del servidor que almacena la base de datos de cuentas de usuario utilizada por un servidor RAS especificado, puede llamar a la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) . Después, puede usar el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios en una base de datos de cuentas de usuario. También puede usar el nombre del servidor en las llamadas a las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obtener y establecer los privilegios ras para una cuenta de usuario especificada.

Las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) usan la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) para especificar los privilegios de Ras y el número de teléfono de devolución de llamada de un usuario. Los privilegios de RAS indican la información siguiente:

-   Si el usuario puede establecer una conexión remota con el servidor o el dominio al que pertenece el servidor.
-   Si el usuario puede establecer una conexión a través de una devolución de llamada, en la que el servidor RAS se cuelga y, a continuación, vuelve a llamar al usuario para establecer la conexión.

Cada cuenta de usuario especifica una de las marcas siguientes para indicar el privilegio de devolución de llamada del usuario.



| Value                      | Significado                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | El servidor RAS no volverá a llamar al usuario para establecer una conexión.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Cuando el usuario llama a, el servidor RAS se cuelga y llama a un número de teléfono de devolución de llamada preestablecido almacenado en la base de datos de cuentas de usuario. El miembro **szPhoneNumber** de la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) contiene el número de teléfono de devolución de llamada del usuario. |
| RASPRIV \_ CallerSetCallback | Cuando el usuario llama a, el servidor RAS ofrece la opción de especificar un número de teléfono de devolución de llamada. El usuario también puede optar por conectarse inmediatamente sin una devolución de llamada. El miembro **szPhoneNumber** contiene un número predeterminado que el usuario puede invalidar.      |



 

 

 