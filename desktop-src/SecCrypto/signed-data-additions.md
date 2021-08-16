---
description: Enumera los cambios en las funcionalidades de los datos firmados.
ms.assetid: 0518a336-d996-4a82-9336-a448284c72dd
title: Adiciones de datos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5e9f1433a432ba3c3a414e11b83e429ad9c0abc7364b5e5b7451f72d886e33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900395"
---
# <a name="signed-data-additions"></a>Adiciones de datos firmados

Se han realizado los siguientes cambios en las funcionalidades de datos firmados:

-   El contenido [*interno que no es*](../secgloss/i-gly.md) de datos se encapsula en una CADENA DE OCTETO.
-   El aprovisionamiento se realiza para distintas versiones de mensajes.
-   Los firmantes se pueden identificar mediante el emisor y el número de serie, como en PKCS \# 7 1.5, o por el identificador de clave del firmante.
-   Se permiten varios firmantes.
-   Se permiten firmas RSA, DSA y ECDSA.
-   Los algoritmos basados en criptografía de curva elíptica (ECC) y AES requieren Windows Vista o posterior.

 

 
