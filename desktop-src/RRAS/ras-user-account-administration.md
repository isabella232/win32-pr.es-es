---
title: Administración de cuentas de usuario ras
description: Un Windows RAS nt 4.0 usa una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6254a2d4066c6b4b4e1f1167ec842cd86c07d8122b0683c985cbea0a8ca7f2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028736"
---
# <a name="ras-user-account-administration"></a>Administración de cuentas de usuario ras

Un Windows RAS nt 4.0 usa una base de datos de cuentas de usuario que contiene información sobre un conjunto de cuentas de usuario. La información incluye los privilegios RAS de un usuario, que son un conjunto de marcas de bits que determinan cómo responde el servidor RAS cuando el usuario llama a para conectarse. Las funciones de administración del servidor RAS permiten localizar la base de datos de la cuenta de usuario y obtener y establecer los privilegios ras para las cuentas de usuario.

Un servidor RAS de Windows NT 4.0 puede formar parte de un dominio Windows NT/Windows 2000, o puede ser un servidor o estación de trabajo de Windows NT independiente que no forma parte de un dominio. Para un servidor que forma parte de un dominio, la base de datos de la cuenta de usuario se almacena en el servidor que es el controlador de dominio principal (PDC). Un servidor independiente almacena su propia base de datos de cuentas de usuario local. Para obtener el nombre del servidor que almacena la base de datos de cuentas de usuario utilizada por un servidor RAS especificado, puede llamar a la [**función RasAdminGetUserAccountServer.**](rasadmingetuseraccountserver.md) A continuación, puede usar el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios de una base de datos de cuentas de usuario. También puede usar el nombre del servidor en las llamadas a las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obtener y establecer los privilegios ras para una cuenta de usuario especificada.

Las [**funciones RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) usan la estructura [**RAS USER \_ \_ 0**](ras-user-0-str.md) para especificar los privilegios RAS de un usuario y el número de teléfono de llamada. Los privilegios ras indican la siguiente información:

-   Si el usuario puede establecer una conexión remota con el servidor o el dominio al que pertenece el servidor.
-   Si el usuario puede establecer una conexión a través de una llamada de vuelta, en la que el servidor RAS se vuelve a cargar y, a continuación, vuelve a llamar al usuario para establecer la conexión.

Cada cuenta de usuario especifica una de las marcas siguientes para indicar el privilegio de dedo de llamada del usuario.



| Value                      | Significado                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | El servidor RAS no llamará al usuario para establecer una conexión.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Cuando el usuario llama a , el servidor RAS se para y llama a un número de teléfono de de vuelta de llamada preestablecido almacenado en la base de datos de la cuenta de usuario. El **miembro szPhoneNumber** de la [**estructura RAS USER \_ \_ 0**](ras-user-0-str.md) contiene el número de teléfono de llamada del usuario. |
| RASPRIV \_ CallerSetCallback | Cuando el usuario llama a , el servidor RAS proporciona la opción de especificar un número de teléfono de de vuelta de llamada. El usuario también puede optar por conectarse inmediatamente sin llamar de nuevo. El **miembro szPhoneNumber** contiene un número predeterminado que el usuario puede invalidar.      |



 

 

 