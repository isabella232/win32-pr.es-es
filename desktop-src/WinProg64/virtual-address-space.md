---
title: Espacio de direcciones virtuales (Guía de programación para Windows de 64 bits)
description: De forma predeterminada, las aplicaciones basadas en Microsoft Windows de 64 bits tienen un espacio de direcciones de modo de usuario de varios terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, espacio de direcciones virtuales
- espacio de direcciones virtuales 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078674"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Espacio de direcciones virtuales (Guía de programación para Windows de 64 bits)

De forma predeterminada, las aplicaciones basadas en Microsoft Windows de 64 bits tienen un espacio de direcciones de modo de usuario de varios terabytes. Para obtener valores precisos, consulte [límites de memoria para las versiones de Windows y Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases). Sin embargo, las aplicaciones pueden especificar que el sistema debe asignar toda la memoria para la aplicación por debajo de 2 gigabytes. Esta característica es útil para las aplicaciones de 64 bits si se cumplen las condiciones siguientes:

-   Un espacio de direcciones de 2 GB es suficiente.
-   El código tiene muchas advertencias de truncamiento de puntero.
-   Los punteros y los enteros se mezclan libremente.
-   El código tiene el polimorfismo usando tipos de datos de 32 bits.

Todos los punteros siguen siendo punteros de 64 bits, pero el sistema garantiza que cada asignación de memoria se produce por debajo del límite de 2 GB, de modo que si la aplicación trunca un puntero, no se pierden datos significativos. Los punteros se pueden truncar en valores de 32 bits y, a continuación, extenderse a valores de 64 bits mediante la extensión de signo o la extensión de cero.

Para especificar esta limitación de memoria, use la opción **/LARGEADDRESSAWARE: sin** enlazador. Tenga en cuenta que **/LARGEADDRESSAWARE: no** se omite para un binario ARM64. Sin embargo, tenga en cuenta que pueden producirse problemas al usar esta opción. Si crea un archivo DLL que usa esta opción y una aplicación que no usa esta opción llama a la DLL, el archivo DLL podría truncar un puntero de 64 bits cuyos bits superiores 32 sean significativos. Esto puede producir un error de la aplicación sin ninguna advertencia.

 

 
