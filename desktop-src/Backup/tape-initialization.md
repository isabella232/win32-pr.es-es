---
title: Inicialización de cinta
description: Una aplicación debe utilizar la función CreateFile para crear un identificador de un dispositivo de cinta. Este identificador se usa en operaciones posteriores en la cinta del dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Copia de seguridad de inicialización de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488002"
---
# <a name="tape-initialization"></a>Inicialización de cinta

Una aplicación debe utilizar la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para crear un identificador de un dispositivo de cinta. Este identificador se usa en operaciones posteriores en la cinta del dispositivo.

Antes de que una aplicación escriba en una cinta, la cinta debe estar formateada según las necesidades de la aplicación y las capacidades de la unidad de cinta que se está usando. La función [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) cambia el formato de una cinta y crea en ella un número determinado de particiones de un tamaño especificado.

La función [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara una cinta para tener acceso a ella o quitarla. Esta función puede cargar, descargar, bloquear o desbloquear una cinta. Esta función también puede tensar la cinta moviendo la cinta hasta el final de la cinta y volviendo al principio.

Para recuperar y establecer información sobre una cinta y una unidad de cinta, una aplicación usa las funciones [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)y [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera información que describe una cinta o una unidad de cinta. La información de la cinta incluye el tipo de cinta, la densidad y el tamaño de bloque; el número de particiones de la cinta; la cantidad de cinta restante; etc. La información de la unidad de cinta incluye el tamaño de bloque predeterminado de la unidad, el número máximo de particiones y las características que se admiten.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) establece el tamaño del bloque de cinta o establece las marcas de la unidad de cinta que indican si la unidad admite la corrección de errores de hardware, la compresión de datos, el relleno de datos o cualquier combinación de los tres.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica si la unidad de cinta está lista para procesar comandos de cinta.

 

 