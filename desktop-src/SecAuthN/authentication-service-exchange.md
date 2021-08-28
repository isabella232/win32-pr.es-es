---
description: El usuario comienza a iniciar sesión en la red escribiendo un nombre de inicio de sesión y una contraseña. El cliente Kerberos de la estación de trabajo del usuario convierte la contraseña en una clave de cifrado y guarda el resultado en una variable de programa.
ms.assetid: fcb3b601-9953-474c-9a08-1fa25706f3d7
title: Intercambio del servicio de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480370dd9fe5d7c5fc10e7979de9d4e7f67f99db3e517e1ec6520a3274ef23c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073295"
---
# <a name="authentication-service-exchange"></a>Intercambio del servicio de autenticación

El usuario comienza a iniciar sesión en la red escribiendo un nombre de inicio de sesión y una contraseña. El [*cliente Kerberos*](/windows/desktop/SecGloss/k-gly) de la estación de trabajo del usuario convierte la contraseña en una clave de cifrado y guarda el resultado en una variable de programa.

A continuación, el cliente solicita credenciales para el servicio de concesión de [*vales*](/windows/desktop/SecGloss/c-gly) (TGS) del [*Centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) enviando al servicio de autenticación del KDC un mensaje de tipo KRB \_ AS REQ (solicitud de servicio de autenticación \_ Kerberos). La primera parte de este mensaje identifica el usuario y el servicio TGS que se solicita. La segunda parte de este mensaje contiene datos de autenticación previa diseñados para demostrar que el usuario conoce la contraseña. Se trata simplemente de un mensaje autenticador cifrado con la [*clave maestra*](/windows/desktop/SecGloss/m-gly) derivada de la contraseña de inicio de sesión del usuario.

Cuando el KDC recibe KRB AS REQ, busca al usuario en su base de datos, obtiene la clave maestra del usuario \_ asociado, descifra los datos de autenticación previa y evalúa la marca de tiempo \_ dentro. Si la marca de tiempo es válida, el KDC puede estar seguro de que los datos de autenticación previa se cifraron con la clave maestra del usuario y, por tanto, que el cliente es original.

Una vez que el KDC ha comprobado la identidad del usuario, crea credenciales que el cliente puede presentar al TGS, como se muestra a continuación:

1.  El KDC inventa una clave de [*sesión de*](/windows/desktop/SecGloss/s-gly) inicio de sesión y cifra una copia con la clave maestra del usuario.
2.  El KDC inserta otra copia de la clave de sesión de inicio de sesión y los datos de autorización del usuario en un vale de concesión de vales (TGT) y cifra el TGT con la propia clave maestra del KDC.
3.  El KDC devuelve estas credenciales al cliente respondiendo con un mensaje de tipo KRB AS REP (respuesta del servicio de \_ \_ autenticación Kerberos).
4.  Cuando el cliente recibe la respuesta, usa la clave derivada de la contraseña del usuario para descifrar la nueva clave de sesión de inicio de sesión.
5.  El cliente almacena la nueva clave en su caché de vales.
6.  El cliente extrae el TGT del mensaje y lo almacena también en su caché de vales.

 

 
