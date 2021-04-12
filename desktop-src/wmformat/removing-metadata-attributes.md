---
title: Quitar atributos de metadatos
description: Quitar atributos de metadatos
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- SDK de Windows Media Format, quitar atributos de metadatos
- Advanced Systems Format (ASF), quitar atributos de metadatos
- ASF (formato de sistemas avanzados), quitar atributos de metadatos
- metadatos, quitar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420445"
---
# <a name="removing-metadata-attributes"></a>Quitar atributos de metadatos

Puede quitar un atributo de metadatos pasando su índice y el número de secuencia al método [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) . El orden en el que se indexan los atributos restantes después de quitar un atributo no cambia; todos los atributos restantes que originalmente tenían un valor de índice mayor que el que se ha quitado tienen sus valores de índice reducidos en uno. Al quitar varios atributos, hágalo en orden descendente por índice para evitar tener que calcular el ajuste en la indexación.

Para mayor comodidad en la eliminación de valores, el método [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) devuelve los valores de índice en orden descendente.

> [!Note]  
> Los valores de índice obtenidos mediante el uso de los métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) no son compatibles con los valores de índice obtenidos mediante los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Si usa los métodos de una interfaz para cambiar los atributos de un archivo, debe suponer que los valores de índice recuperados previamente de la otra interfaz ya no son válidos y se deben obtener de nuevo. Debe evitar el uso de los métodos de **IWMHeaderInfo** si es posible.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




