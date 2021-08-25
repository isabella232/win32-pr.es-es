---
description: Enumera los cambios en las funcionalidades para envolver los datos.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Adiciones de datos sobres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75aab8e931ff8c8591a899a21a1071754e32f2e2cecec3755baa3dc64db94dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874425"
---
# <a name="enveloped-data-additions"></a>Adiciones de datos sobres

Se han realizado los siguientes cambios en las funcionalidades de datos envolventes:

-   La identificación del destinatario puede realizarse no solo por el emisor y el número de serie (PKCS \# 7 1.5), sino también por el identificador de clave.
-   Se proporcionan tres opciones de intercambio de claves de destinatario:
    -   Transporte de claves mediante claves RSA.
    -   Acuerdo de clave mediante Ephemeral-Static Diffie-Hellman claves de algoritmo encapsuladas con 3DES o RC2, o Ephemeral-Static curva elíptica Diffie-Hellman claves de algoritmo encapsuladas con AES.
    -   Clave de cifrado de claves o transferencia de claves de lista de correo donde la clave usada para cifrar la clave de cifrado de contenido ya se ha distribuido a los destinatarios. RC2, 3DES y AES se permiten como algoritmos de ajuste de claves.
-   Los atributos no protegido se pueden incluir en el mensaje.
-   Se ha agregado un campo **OriginatorInfo** que contiene información sobre el originador que puede contener certificados y CRL.
-   Los algoritmos basados en criptografía de curva elíptica (ECC) y AES requieren Windows Vista o posterior.

 

 



