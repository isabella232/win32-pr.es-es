---
title: Recuperar atributos de metadatos
description: Recuperar atributos de metadatos
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows SDK de formato multimedia, recuperación de atributos de metadatos
- Formato de sistemas avanzados (ASF), recuperación de atributos de metadatos
- ASF (formato de sistemas avanzados), recuperación de atributos de metadatos
- metadata,retrieving attributes
- streams,retrieving metadata attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360206"
---
# <a name="retrieving-metadata-attributes"></a>Recuperar atributos de metadatos

Para recuperar un atributo de un encabezado de archivo, debe conocer el número de secuencia y el índice del atributo. Puede usar el método [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) para obtener los índices de todos los atributos con el mismo nombre o todos los índices en el mismo lenguaje. Al igual que los demás métodos de [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) **GetAttributeIndices** trata con una sola secuencia o con todos los atributos de nivel de archivo mediante el flujo 0. Puede usar 0xFFFF para el número de secuencia para obtener índices globales que coincidan con los criterios de todo el archivo, independientemente del número de secuencia.

Cuando conozca el índice del atributo que desea recuperar, llame a [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) para obtener el atributo. Debe realizar dos llamadas a **GetAttributeByIndexEx** para cada atributo recuperado. En la primera llamada, pase **NULL para** el nombre y los punteros del búfer de datos para obtener el tamaño necesario. A continuación, asigne búferes del tamaño indicado y realice la segunda llamada para recuperar el nombre y los datos.

Para obtener código de ejemplo que muestra cómo recuperar atributos de metadatos, vea [Para recuperar todos los metadatos de un archivo](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




