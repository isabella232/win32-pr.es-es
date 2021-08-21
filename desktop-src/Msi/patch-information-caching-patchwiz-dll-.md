---
description: La generación de una nueva revisión puede requerir mucho tiempo.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Almacenamiento en caché de información de revisión (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71513ea1a9418506bbf9025f66a1689c12e9a53f8e6f2e713ddeb3b3d55de580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942626"
---
# <a name="patch-information-caching-patchwizdll"></a>Almacenamiento en caché de información de revisión (Patchwiz.dll)

La generación de una nueva revisión puede requerir mucho tiempo. Después de haber generado una revisión [ mediantePatchwiz.dll](patchwiz-dll.md), es posible que deba cambiar la imagen de actualización de nuevo y generar otra revisión. El almacenamiento en caché de información de revisión puede reducir el tiempo necesario para generar revisiones posteriores mediante la reusación de las revisiones existentes. Por ejemplo, el tiempo necesario para crear Service Pack se puede reducir mediante las revisiones binarias generadas a partir de revisiones anteriores. Patchwiz.dll puede usar PATCH CACHE DIR para buscar una revisión binaria existente y agregarla al gabinete del Service Pack sin tener que volver a crear \_ \_ la revisión binaria.

El almacenamiento en caché de información de revisión requiere el [ uso dePatchwiz.dll](patchwiz-dll.md). Para activar el almacenamiento en caché de revisiones, establezca las propiedades PATCH CACHE ENABLED y PATCH CACHE DIR en la Tabla de propiedades (Patchwiz.dll) del archivo de propiedades de creación de revisiones \_ \_ \_ \_ (archivo .ijo). [](properties-table-patchwiz-dll-.md) Patchwiz almacena toda la información de creación de revisiones en la carpeta identificada por la propiedad PATCH CACHE DIR y \_ crea esta carpeta si es \_ necesario. La próxima vez que intente crear una revisión, Patchwiz comprueba esta carpeta para ver si los archivos que se compararán coinciden con los archivos de la memoria caché. Si los archivos coinciden, Patchwiz usa la información almacenada en caché en lugar de volver a generar la revisión binaria para el archivo. Si los archivos no coinciden o falta la información de la memoria caché, Patchwiz genera la revisión para el archivo.

Para usar el almacenamiento en caché de información de revisión, la carpeta especificada por PATCH CACHE DIR debe conservarse \_ después de crear un archivo \_ .msp. Si se elimina la carpeta, PatchWiz tiene que volver a generar revisiones binarias para los archivos .msp posteriores. Para obtener más información sobre cómo conservar información en las regiones seleccionadas de un archivo de destino, vea Aplicar revisiones a [las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md).

 

 



