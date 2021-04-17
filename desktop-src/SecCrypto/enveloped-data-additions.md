---
description: Enumera los cambios en las capacidades para la protección de datos.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adiciones de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666949"
---
# <a name="enveloped-data-additions"></a>Adiciones de datos con doble cifrado

Se han realizado los siguientes cambios en las capacidades de datos con doble cifrado:

-   La identificación de destinatarios solo puede realizarse mediante el emisor y el número de serie (PKCS \# 7 1,5), pero también con el identificador de clave.
-   Se proporcionan tres opciones de intercambio de claves de destinatario:
    -   Transporte de claves mediante claves RSA.
    -   Acuerdo de claves mediante Ephemeral-Static Diffie-Hellman las claves de algoritmo encapsuladas con 3DES o RC2, o Ephemeral-Static las claves de algoritmo Diffie-Hellman de curva elíptica encapsuladas con AES.
    -   Clave de cifrado de claves o transferencia de clave de lista de correo en la que la clave usada para cifrar la clave de cifrado de contenido ya se ha distribuido a los destinatarios. RC2, 3DES y AES se permiten como algoritmos de ajuste de clave.
-   Los atributos no protegidos pueden incluirse en el mensaje.
-   Se ha agregado un campo **OriginatorInfo** que contiene información sobre el originador que puede contener certificados y CRL.
-   Los algoritmos basados en criptografía de curva elíptica (ECC) y AES requieren Windows Vista o posterior.

 

 



