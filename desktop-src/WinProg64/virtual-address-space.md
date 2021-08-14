---
title: Espacio de direcciones virtuales (Guía de programación para aplicaciones de 64 Windows)
description: De forma predeterminada, las aplicaciones basadas Windows microsoft de 64 bits tienen un espacio de direcciones en modo de usuario de varios terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guía de programación de 64 Windows de programación de 64 Windows programación, espacio de direcciones virtuales
- Espacio de direcciones virtuales de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2e673befb66c45501558effb37f3d04ee1a99199010f8cca89abb2cb31c6d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113375"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Espacio de direcciones virtuales (Guía de programación para aplicaciones de 64 Windows)

De forma predeterminada, las aplicaciones basadas Windows microsoft de 64 bits tienen un espacio de direcciones en modo de usuario de varios terabytes. Para obtener valores precisos, vea [Límites](/windows/desktop/Memory/memory-limits-for-windows-releases)de memoria para Windows y Windows versiones de servidor . Sin embargo, las aplicaciones pueden especificar que el sistema debe asignar toda la memoria para la aplicación por debajo de 2 gigabytes. Esta característica es beneficiosa para las aplicaciones de 64 bits si se cumplen las condiciones siguientes:

-   Un espacio de direcciones de 2 GB es suficiente.
-   El código tiene muchas advertencias de truncamiento de puntero.
-   Los punteros y los enteros se mezclan libremente.
-   El código tiene polimorfismo mediante tipos de datos de 32 bits.

Todos los punteros siguen siendo punteros de 64 bits, pero el sistema garantiza que cada asignación de memoria se produce por debajo del límite de 2 GB, por lo que si la aplicación trunca un puntero, no se pierden datos significativos. Los punteros se pueden truncar a valores de 32 bits y luego extenderse a valores de 64 bits mediante la extensión de signo o la extensión cero.

Para especificar esta limitación de memoria, use **la opción /LARGEADDRESSAWARE:NO** del vinculador. Tenga en **cuenta que /LARGEADDRESSAWARE:NO se** omite para un binario arm64. Sin embargo, tenga en cuenta que pueden producirse problemas al usar esta opción. Si compila un archivo DLL que usa esta opción y una aplicación que no usa esta opción llama al archivo DLL, el archivo DLL podría truncar un puntero de 64 bits cuyos 32 bits superiores sean significativos. Esto puede provocar un error en la aplicación sin ninguna advertencia.

 

 
