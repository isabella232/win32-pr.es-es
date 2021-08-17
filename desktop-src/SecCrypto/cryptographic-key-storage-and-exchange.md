---
description: Hay situaciones en las que las claves deben exportarse desde el entorno seguro del proveedor de servicios criptográficos (CSP) al espacio de datos de una aplicación. Las claves que se han exportado se almacenan en estructuras blob de clave cifradas.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Clave criptográfica Storage y Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3028efb449b59deb24a7097369d8894d0876907f3555c836e95e14d8c4bf5cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768762"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Clave criptográfica Storage y Exchange

Hay situaciones en las que las claves [](../secgloss/c-gly.md) deben exportarse desde el entorno seguro del proveedor de servicios criptográficos (CSP) al espacio de datos de una aplicación. Las claves que se han exportado se almacenan en estructuras [*blob de clave cifradas.*](../secgloss/k-gly.md)

Hay dos situaciones específicas en las que es necesario exportar claves:

-   Para guardar una [*clave de sesión*](../secgloss/s-gly.md) para su uso posterior por una aplicación, si, por ejemplo, una aplicación acaba de cifrar un archivo de base de datos para descifrarlo más adelante. La aplicación es responsable de almacenar la clave de cifrado. Esto es necesario porque los CSP no conservan las [*claves simétricas*](../secgloss/s-gly.md) de una sesión a otra.
-   Para enviar una clave a otra persona. Esto sería más fácil si los respectivos CSP pudieran comunicarse directamente, pero no. Dado que los CSP no se pueden comunicar, la clave debe exportarse desde un CSP, transmitirse a la aplicación de destino y, a continuación, importarse en el CSP de destino. Este proceso puede ser más complicado si la ruta de comunicación no es de confianza.

En cualquier caso, una aplicación debe almacenar una clave de sesión fuera del CSP durante un período de tiempo. Para obtener más información, [vea Procedimiento para almacenar una clave de sesión.](procedure-for-storing-a-session-key.md)

 

 
