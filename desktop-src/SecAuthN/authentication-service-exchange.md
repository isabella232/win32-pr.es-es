---
description: El usuario comienza a iniciar sesión en la red escribiendo un nombre de inicio de sesión y una contraseña. El cliente Kerberos de la estación de trabajo del usuario convierte la contraseña en una clave de cifrado y guarda el resultado en una variable de programa.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Intercambio del servicio de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14121ed33ae0ac169c590b03dfb0b395306d11f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648467"
---
# <a name="authentication-service-exchange"></a>Intercambio del servicio de autenticación

El usuario comienza a iniciar sesión en la red escribiendo un nombre de inicio de sesión y una contraseña. El cliente [*Kerberos*](/windows/desktop/SecGloss/k-gly) de la estación de trabajo del usuario convierte la contraseña en una clave de cifrado y guarda el resultado en una variable de programa.

A continuación, el cliente solicita [*las credenciales*](/windows/desktop/SecGloss/c-gly) para el servicio de concesión de vales (TGS) del [*centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) mediante el envío del servicio de autenticación del KDC a un mensaje de tipo KRB \_ como \_ req (solicitud del servicio de autenticación de Kerberos). La primera parte de este mensaje identifica al usuario y al servicio TGS que se solicita. La segunda parte de este mensaje contiene datos de autenticación previa para demostrar que el usuario conoce la contraseña. Esto es simplemente un mensaje de autenticador que se cifra con la [*clave maestra*](/windows/desktop/SecGloss/m-gly) derivada de la contraseña de inicio de sesión del usuario.

Cuando el KDC recibe KRB \_ como \_ req, busca el usuario en su base de datos, obtiene la clave maestra del usuario asociada, descifra los datos de autenticación previa y evalúa la marca de tiempo dentro de. Si la marca de tiempo es válida, el KDC puede estar seguro de que los datos de autenticación previa se cifraron con la clave maestra del usuario y, por tanto, de que el cliente es auténtico.

Una vez que el KDC ha comprobado la identidad del usuario, crea las credenciales que el cliente puede presentar al TGS, como se indica a continuación:

1.  El KDC invent una clave de [*sesión*](/windows/desktop/SecGloss/s-gly) de inicio de sesión y cifra una copia con la clave maestra del usuario.
2.  El KDC inserta otra copia de la clave de sesión de inicio de sesión y los datos de autorización del usuario en un vale de concesión de vales (TGT) y cifra el TGT con la clave maestra propia del KDC.
3.  El KDC envía estas credenciales de vuelta al cliente respondiendo con un mensaje de tipo KRB \_ como \_ REP (respuesta del servicio de autenticación Kerberos).
4.  Cuando el cliente recibe la respuesta, utiliza la clave derivada de la contraseña del usuario para descifrar la nueva clave de la sesión de inicio de sesión.
5.  El cliente almacena la nueva clave en su caché de vales.
6.  El cliente extrae el TGT del mensaje y lo almacena también en su caché de vales.

 

 
