---
title: Inicialización de cintas
description: Una aplicación debe usar la función CreateFile para crear un identificador de un dispositivo de cinta. Este identificador se usa en operaciones posteriores en la cinta del dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- copia de seguridad de inicialización de cintas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aeba729feb9351b5af15d26f6366b455c5ce74a9cc6300c9ab8d25047b4760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835408"
---
# <a name="tape-initialization"></a>Inicialización de cintas

Una aplicación debe usar la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para crear un identificador de un dispositivo de cinta. Este identificador se usa en operaciones posteriores en la cinta del dispositivo.

Antes de que una aplicación escriba en una cinta, se debe dar formato a la cinta según las necesidades de la aplicación y las funcionalidades de la unidad de cinta que se usa. La [**función CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) vuelve a formatear una cinta y crea en ella un número determinado de particiones de un tamaño especificado.

La [**función PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara una cinta a la que se va a acceder o quitar. Esta función puede cargar, descargar, bloquear o desbloquear una cinta. Esta función también puede desplazar la cinta al final de la cinta y volver al principio.

Para recuperar y establecer información sobre una unidad de cinta y cinta, una aplicación usa las funciones [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)y [**GetTapeStatus.**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera información que describe una cinta o una unidad de cinta. La información de cinta incluye el tipo, la densidad y el tamaño de bloque de la cinta. el número de particiones en la cinta; la cantidad de cinta restante; y así sucesivamente. La información de la unidad de cinta incluye el tamaño de bloque predeterminado de la unidad, el número máximo de particiones y las características que se admiten.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) establece el tamaño del bloque de cinta o establece las marcas de unidad de cinta que indican si la unidad admite la corrección de errores de hardware, la compresión de datos, el relleno de datos o cualquier combinación de los tres.

[**GetTapeStatus indica**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) si la unidad de cinta está lista para procesar comandos de cinta.

 

 