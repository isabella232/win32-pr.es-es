---
description: Como el protocolo Kerberos se diseñó originalmente, una clave maestra para un usuario se derivó de una contraseña proporcionada por el usuario.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket-Granting vales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dff161ba2d905f676fe6b6b5e7e7d5289ee550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154344"
---
# <a name="ticket-granting-tickets"></a>Ticket-Granting vales

Como el [*protocolo Kerberos*](../secgloss/k-gly.md) se diseñó originalmente, una clave maestra para un usuario se derivó de una contraseña proporcionada por el usuario. Cuando un usuario ha iniciado sesión, el cliente Kerberos de la estación de trabajo del usuario aceptó la contraseña del usuario y la ha convertido en una clave de cifrado pasando el texto a través de una función [*hash*](../secgloss/h-gly.md) unidireccional. El hash resultante era la [*clave maestra*](../secgloss/m-gly.md)del usuario. El cliente usó esta *clave maestra* para descifrar [*las claves de sesión*](../secgloss/s-gly.md) recibidas de KDC.

El problema con el diseño de Kerberos original es que el cliente necesita la clave maestra del usuario cada vez que descifra una clave de sesión del KDC. Esto significa que el cliente debe pedir al usuario la contraseña al principio de cada intercambio cliente/servidor, o bien el cliente debe almacenar la clave del usuario en la estación de trabajo. Las interrupciones frecuentes del usuario son demasiado intrusivas. El almacenamiento de la clave en la estación de trabajo pone en peligro una clave derivada de la contraseña del usuario, que es una clave a largo plazo.

La solución del protocolo Kerberos a este problema es que el cliente obtenga una clave temporal del KDC. Esta clave temporal solo es adecuada para esta [*sesión de inicio*](../secgloss/l-gly.md)de sesión. Cuando un usuario inicia sesión, el cliente solicita un vale para el KDC de la misma forma que solicitaría un vale para cualquier otro servicio. El KDC responde mediante la creación de una clave de sesión de inicio de sesión y un vale para un servidor especial, el servicio de concesión de vales completo del KDC. En el vale se inserta una copia de la clave de sesión de inicio de sesión y el vale se cifra con la clave maestra del KDC. Otra copia de la clave de sesión de inicio de sesión se cifra con la clave maestra del usuario derivada de la contraseña de inicio de sesión del usuario. Tanto el vale como la clave de sesión cifrada se envían al cliente.

Cuando el cliente obtiene la respuesta del KDC, descifra la clave de sesión de inicio de sesión con la clave maestra del usuario derivada de la contraseña del usuario. El cliente ya no necesita la clave derivada de la contraseña del usuario, ya que ahora el cliente usará la clave de sesión de inicio de sesión para descifrar su copia de cualquier clave de sesión de servidor que obtenga del KDC. El cliente almacena la clave de sesión de inicio de sesión en su caché de vales junto con su vale para el servicio de concesión de vales completo del KDC.

El vale del servicio de concesión de vales completo se denomina vale de concesión de vales (TGT). Cuando el cliente solicita al KDC un vale para un servidor, presenta [*credenciales*](../secgloss/c-gly.md) en forma de mensaje de autenticador y un vale, en este caso un TGT, de la misma forma que presenta las credenciales a cualquier otro servicio. El servicio de concesión de vales abre el TGT con su clave maestra, extrae la clave de sesión de inicio de sesión para este cliente y usa la clave de sesión de inicio de sesión para cifrar la copia del cliente de una clave de sesión del servidor.

 

 
