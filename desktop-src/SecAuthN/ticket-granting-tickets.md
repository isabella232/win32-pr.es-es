---
description: Como el protocolo Kerberos se diseñó originalmente, una clave maestra para un usuario se derivaba de una contraseña proporcionada por el usuario.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket-Granting Tickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd56ef05ce2ea9149b9bd35ef17dc684973f7125026f474e5a8dd3d1d14ff4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916387"
---
# <a name="ticket-granting-tickets"></a>Ticket-Granting Tickets

Como el [*protocolo Kerberos se*](../secgloss/k-gly.md) diseñó originalmente, una clave maestra para un usuario se derivaba de una contraseña proporcionada por el usuario. Cuando un usuario ha iniciado sesión, el cliente Kerberos de la estación de trabajo del usuario aceptó la contraseña del usuario y la convirtió en una clave de cifrado pasando el texto a través de una función [*hash*](../secgloss/h-gly.md) unida. El hash resultante era la clave maestra [*del usuario.*](../secgloss/m-gly.md) El cliente usó esta *clave maestra para* descifrar las claves de sesión [*recibidas*](../secgloss/s-gly.md) de KDC.

El problema con el diseño kerberos original es que el cliente necesita la clave maestra del usuario cada vez que descifra una clave de sesión del KDC. Esto significa que el cliente debe pedir al usuario la contraseña al principio de cada intercambio cliente/servidor, o bien el cliente debe almacenar la clave del usuario en la estación de trabajo. Las interrupciones frecuentes del usuario son demasiado intrusivas. Almacenar la clave en la estación de trabajo corre el riesgo de poner en peligro una clave derivada de la contraseña de usuario que es una clave a largo plazo.

La solución del protocolo Kerberos a este problema es que el cliente obtenga una clave temporal del KDC. Esta clave temporal solo es buena para esta sesión [*de inicio de sesión.*](../secgloss/l-gly.md) Cuando un usuario inicia sesión, el cliente solicita un vale para el KDC igual que solicitaría un vale para cualquier otro servicio. El KDC responde mediante la creación de una clave de sesión de inicio de sesión y un vale para un servidor especial, el servicio de concesión de vales completo del KDC. Se inserta una copia de la clave de sesión de inicio de sesión en el vale y el vale se cifra con la clave maestra del KDC. Otra copia de la clave de sesión de inicio de sesión se cifra con la clave maestra del usuario derivada de la contraseña de inicio de sesión del usuario. Tanto el vale como la clave de sesión cifrada se envían al cliente.

Cuando el cliente obtiene la respuesta del KDC, descifra la clave de sesión de inicio de sesión con la clave maestra del usuario derivada de la contraseña del usuario. El cliente ya no necesita la clave derivada de la contraseña del usuario porque el cliente usará ahora la clave de sesión de inicio de sesión para descifrar su copia de cualquier clave de sesión del servidor que obtiene del KDC. El cliente almacena la clave de sesión de inicio de sesión en su caché de vales junto con su vale para el servicio de concesión de vales completo del KDC.

El vale para el servicio de concesión de vales completo se denomina vale de concesión de vales (TGT). Cuando el cliente solicita al KDC un vale [](../secgloss/c-gly.md) a un servidor, presenta las credenciales en forma de mensaje de autenticador y un vale (en este caso, un TGT), igual que presentaría las credenciales a cualquier otro servicio. El servicio de concesión de vales abre el TGT con su clave maestra, extrae la clave de sesión de inicio de sesión para este cliente y usa la clave de sesión de inicio de sesión para cifrar la copia del cliente de una clave de sesión para el servidor.

 

 
