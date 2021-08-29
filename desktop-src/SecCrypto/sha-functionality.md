---
description: El proveedor base original informó incorrectamente de que el algoritmo hash SHA enumeraba algoritmos mediante llamadas a CryptGetProvParam con el parámetro PP \_ ENUMALGS especificado.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funcionalidad sha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728415b746681121593a3e93f62a66168e59ca49b6f7737b6f39565ba00200d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900336"
---
# <a name="sha-functionality"></a>Funcionalidad sha

El proveedor base original informó incorrectamente de que el algoritmo hash [*SHA*](../secgloss/s-gly.md) enumeraba algoritmos mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el parámetro PP \_ ENUMALGS especificado. Esto se ha corregido en el proveedor base. Tanto el proveedor base revisado como el proveedor extendido y ahora informan correctamente de SHA-1.

Se ha agregado una constante CALG SHA1 definida a \_ Wincrypt.h con el mismo valor que CALG \_ SHA.

 

 
