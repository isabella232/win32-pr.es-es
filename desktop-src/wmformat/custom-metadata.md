---
title: Metadatos personalizados
description: Metadatos personalizados
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows SDK de formato multimedia, metadatos personalizados
- Formato de sistemas avanzados (ASF), metadatos personalizados
- ASF (formato de sistemas avanzados), metadatos personalizados
- Windows SDK de formato multimedia, interfaz IWMHeaderInfo3
- Advanced Systems Format (ASF), interfaz IWMHeaderInfo3
- ASF (formato de sistemas avanzados), interfaz IWMHeaderInfo3
- metadata,customizing
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbbc9fdfc07500e43a3a3875bbb62a77ed176df7a1607a6cb902cef24160e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809455"
---
# <a name="custom-metadata"></a>Metadatos personalizados

Además de los muchos atributos admitidos que se proporcionan con el SDK Windows Media Format, puede crear atributos de metadatos según sus propias especificaciones. Al crear atributos de metadatos personalizados, debe usar una convención de nomenclatura fácilmente identificable para evitar posibles conflictos con los atributos creados por otros.

Se recomienda usar los métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para crear los metadatos debido a la flexibilidad agregada que proporcionan sobre los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Características de metadatos**](metadata-features.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




