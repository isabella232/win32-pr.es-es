---
description: La generación de una nueva revisión puede requerir mucho tiempo.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Almacenamiento en caché de información de revisión (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7000efceea62e9eef122a34f7700622e1e6e2e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652523"
---
# <a name="patch-information-caching-patchwizdll"></a>Almacenamiento en caché de información de revisión (Patchwiz.dll)

La generación de una nueva revisión puede requerir mucho tiempo. Una vez que haya generado una revisión mediante [Patchwiz.dll](patchwiz-dll.md), puede que tenga que volver a cambiar la imagen de actualización y generar otra revisión. El almacenamiento en caché de información de revisiones puede reducir el tiempo necesario para generar revisiones posteriores mediante la reutilización de las revisiones existentes. Por ejemplo, el tiempo necesario para crear los Service Packs se puede reducir mediante el uso de revisiones binarias generadas a partir de revisiones anteriores. Patchwiz.dll puede usar \_ \_ el directorio de la caché de revisión para buscar una revisión binaria existente y agregarla al archivo. cab del Service Pack sin tener que volver a crear la revisión binaria.

El almacenamiento en caché de información de revisión requiere el uso de [Patchwiz.dll](patchwiz-dll.md). Para activar el almacenamiento en caché de la revisión, establezca las propiedades de la \_ caché \_ de revisión habilitada y del \_ \_ Directorio de la caché de revisión en la [tabla de propiedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) del archivo de propiedades de creación de revisiones (archivo. PCP). Patchwiz almacena toda la información de creación de revisiones en la carpeta identificada por la \_ propiedad de directorio patch cache \_ y crea esta carpeta si es necesario. La próxima vez que intente crear una revisión, Patchwiz comprueba esta carpeta para ver si los archivos que se van a comparar coinciden con los archivos de la memoria caché. Si los archivos coinciden, Patchwiz usa la información almacenada en caché en lugar de volver a generar la revisión binaria del archivo. Si los archivos no coinciden, o si falta la información de la memoria caché, Patchwiz genera la revisión para el archivo.

Para usar el almacenamiento en caché de la información de revisión, la carpeta especificada por PATCH \_ Cache \_ dir debe conservarse después de crear un archivo. msp. Si se elimina la carpeta, PatchWiz tiene que volver a generar revisiones binarias para los archivos. MSP posteriores. Para obtener más información sobre cómo conservar información en las regiones seleccionadas de un archivo de destino, consulte [aplicar revisiones a las regiones seleccionadas de un archivo](patching-selected-regions-of-a-file.md).

 

 



