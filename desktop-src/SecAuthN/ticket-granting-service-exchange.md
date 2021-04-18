---
description: Una vez que se ha establecido un vale de concesión de vales (TGT) y una clave de sesión para el cliente, el cliente puede solicitar una clave de sesión independiente y un vale para el servicio.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Intercambio del servicio de concesión de vales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666826"
---
# <a name="ticket-granting-service-exchange"></a>Intercambio del servicio de concesión de vales

Una vez que se ha establecido un vale de concesión de vales (TGT) y una [*clave de sesión*](../secgloss/s-gly.md) para el cliente, el cliente puede solicitar una clave de sesión independiente y un vale para el servicio.

**Para solicitar un vale para otro servicio**

1.  El cliente Kerberos de la estación de trabajo del usuario solicita [*credenciales*](../secgloss/c-gly.md) para el servicio mediante el envío del [*centro de distribución de claves*](../secgloss/k-gly.md) (KDC), un mensaje de tipo KRB \_ TGS \_ req (solicitud de servicio de Kerberos Ticket-Granting). Este mensaje consta de la identidad del servicio para el que el cliente solicita credenciales, un mensaje de autenticador cifrado con la nueva clave de [*sesión*](../secgloss/s-gly.md)de inicio de sesión del usuario y el TGT obtenido del [intercambio del servicio de autenticación](authentication-service-exchange.md).
2.  Cuando el KDC recibe un req de KRB \_ TGS \_ , el KDC descifra el TGT con su clave secreta y extrae la clave de sesión de inicio de sesión del usuario.
3.  El KDC usa la [*clave de sesión*](../secgloss/s-gly.md) de inicio de sesión para descifrar el mensaje del autenticador del usuario y lo evalúa. Si el autenticador pasa la prueba, el KDC extrae los datos de autorización del usuario del TGT e invent una clave de sesión para que el usuario lo comparta con el servidor solicitado.
4.  El KDC cifra una copia de la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario.
5.  El KDC inserta otra copia de la clave de sesión de servicio en un vale, junto con los datos de autorización del usuario, y cifra el vale con la [*clave maestra*](../secgloss/m-gly.md)del servidor.
6.  El KDC envía estas credenciales de vuelta al cliente respondiendo con un mensaje de tipo KRB \_ TGS \_ REP (respuesta del servicio de Kerberos Ticket-Granting).
7.  Cuando el cliente recibe la respuesta, descifra la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario y almacena la clave de sesión de servicio en su caché de vales.
8.  El cliente extrae el vale en el servidor y lo almacena en su caché de vales.

 

 
