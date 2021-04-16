---
description: Hay situaciones en las que las claves se deben exportar desde el entorno seguro del proveedor de servicios criptográficos (CSP) al espacio de datos de una aplicación. Las claves que se han exportado se almacenan en estructuras BLOB de clave cifrada.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Almacenamiento de claves criptográficas y Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666417"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Almacenamiento de claves criptográficas y Exchange

Hay situaciones en las que las claves se deben exportar desde el entorno seguro del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) al espacio de datos de una aplicación. Las claves que se han exportado se almacenan en estructuras [*BLOB de clave*](../secgloss/k-gly.md) cifrada.

Hay dos situaciones específicas en las que es necesario exportar claves:

-   Para guardar una [*clave de sesión*](../secgloss/s-gly.md) para su uso posterior por parte de una aplicación, si, por ejemplo, una aplicación acaba de cifrar un archivo de base de datos para descifrarlo más adelante. La aplicación es responsable de almacenar la clave de cifrado. Esto es necesario porque los CSP no conservan [*las claves simétricas*](../secgloss/s-gly.md) de la sesión en la sesión.
-   Para enviar una clave a otra persona. Esto sería más fácil si los CSP correspondientes pudieran comunicarse directamente, pero no. Dado que los CSP no se pueden comunicar, la clave debe exportarse de un CSP, transmitirse a la aplicación de destino y, a continuación, importarse en el CSP de destino. Este proceso puede ser más complicado si la ruta de comunicación no es de confianza.

En cualquier caso, una aplicación debe almacenar una clave de sesión fuera del CSP durante un período de tiempo. Para obtener más información, consulte [procedimiento para almacenar una clave de sesión](procedure-for-storing-a-session-key.md).

 

 
