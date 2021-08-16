---
title: Recuperar atributos de metadatos
description: Recuperar atributos de metadatos
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows SDK de formato multimedia, recuperación de atributos de metadatos
- Formato de sistemas avanzados (ASF), recuperación de atributos de metadatos
- ASF (formato de sistemas avanzados), recuperación de atributos de metadatos
- metadata,retrieving attributes
- streams,retrieving metadata attributes (secuencias, recuperación de atributos de metadatos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dc24f06779c12d40a109c1a8ef0fee9811370d3459f3811c0c870ee535d749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807885"
---
# <a name="retrieving-metadata-attributes"></a>Recuperar atributos de metadatos

Para recuperar un atributo de un encabezado de archivo, debe conocer el número de secuencia y el índice del atributo. Puede usar el método [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obtener los índices de todos los atributos con el mismo nombre o todos los índices del mismo lenguaje. Al igual que los otros métodos de [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) **GetAttributeIndices** trata con una sola secuencia o con todos los atributos de nivel de archivo mediante el flujo 0. Puede usar 0xFFFF número de secuencia para obtener índices globales que coincidan con los criterios de todo el archivo, independientemente del número de secuencia.

Cuando conozca el índice del atributo que desea recuperar, llame a [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obtener el atributo. Debe realizar dos llamadas a **GetAttributeByIndexEx para** cada atributo recuperado. En la primera llamada, pase **NULL para** el nombre y los punteros de búfer de datos para obtener el tamaño necesario. A continuación, asigne búferes del tamaño indicado y realice la segunda llamada para recuperar el nombre y los datos.

Para obtener código de ejemplo que muestra cómo recuperar atributos de metadatos, vea [Para recuperar todos los metadatos de un archivo](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




