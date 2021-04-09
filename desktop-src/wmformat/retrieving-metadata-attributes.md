---
title: Recuperación de atributos de metadatos
description: Recuperación de atributos de metadatos
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- SDK de Windows Media Format, recuperar atributos de metadatos
- Advanced Systems Format (ASF), recuperar atributos de metadatos
- ASF (formato de sistemas avanzados), recuperar atributos de metadatos
- metadatos, recuperar atributos
- flujos, recuperar atributos de metadatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077280"
---
# <a name="retrieving-metadata-attributes"></a>Recuperación de atributos de metadatos

Para recuperar un atributo de un encabezado de archivo, debe conocer el número de secuencia y el índice del atributo. Puede usar el método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obtener los índices de todos los atributos con el mismo nombre o con todos los índices en el mismo idioma. Al igual que los demás métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** trabaja con un solo flujo o con todos los atributos de nivel de archivo mediante la secuencia 0. Puede usar 0xFFFF para el número de secuencia con el fin de obtener índices globales que coincidan con los criterios en todo el archivo, independientemente del número de secuencia.

Cuando conozca el índice del atributo que desea recuperar, llame a [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obtener el atributo. Debe realizar dos llamadas a **GetAttributeByIndexEx** para cada atributo recuperado. En la primera llamada, pase **null** para los punteros de nombre y de búfer de datos para obtener el tamaño necesario. A continuación, asigne los búferes del tamaño indicado y realice la segunda llamada para recuperar el nombre y los datos.

Para obtener un ejemplo de código que muestra cómo recuperar los atributos de metadatos, vea [para recuperar todos los metadatos de un archivo](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




