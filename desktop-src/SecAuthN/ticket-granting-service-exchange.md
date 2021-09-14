---
description: Una vez que se han establecido un vale de concesión de vales (TGT) y una clave de sesión para el cliente, el cliente puede solicitar una clave de sesión y un vale independientes para el servicio.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Intercambio del servicio de concesión de vales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160950"
---
# <a name="ticket-granting-service-exchange"></a>Intercambio del servicio de concesión de vales

Una vez que se han establecido [](../secgloss/s-gly.md) un vale de concesión de vales (TGT) y una clave de sesión para el cliente, el cliente puede solicitar una clave de sesión y un vale independientes para el servicio.

**Para solicitar un vale para otro servicio**

1.  El cliente Kerberos de la estación [](../secgloss/c-gly.md) de trabajo del usuario solicita credenciales para el servicio mediante el envío, a [*Centro de distribución de claves*](../secgloss/k-gly.md) (KDC), de un mensaje de tipo KRB \_ TGS REQ (solicitud de servicio Ticket-Granting \_ Kerberos). Este mensaje consta de la identidad del servicio para el que el cliente solicita credenciales, [](../secgloss/s-gly.md)un mensaje autenticador cifrado con la nueva clave de sesión de inicio de sesión del usuario y el TGT obtenido del servicio de autenticación [Exchange](authentication-service-exchange.md).
2.  Cuando el KDC recibe un KRB \_ TGS REQ, el KDC descifra el TGT con su clave secreta y extrae la clave de sesión de inicio de sesión \_ del usuario.
3.  El KDC usa la clave de [*sesión de inicio de sesión*](../secgloss/s-gly.md) para descifrar el mensaje autenticador del usuario y lo evalúa. Si el autenticador supera la prueba, el KDC extrae los datos de autorización del usuario del TGT e inventará una clave de sesión para que el usuario la comparta con el servidor solicitado.
4.  El KDC cifra una copia de la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario.
5.  El KDC inserta otra copia de la clave de sesión de servicio en un vale, junto con los datos de autorización del usuario, y cifra el vale con la clave maestra [*del servidor*](../secgloss/m-gly.md).
6.  El KDC devuelve estas credenciales al cliente respondiendo con un mensaje de tipo KRB \_ TGS \_ REP (Kerberos Ticket-Granting Service Reply).
7.  Cuando el cliente recibe la respuesta, descifra la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario y almacena la clave de sesión de servicio en su caché de vales.
8.  El cliente extrae el vale al servidor y lo almacena en su caché de vales.

 

 
