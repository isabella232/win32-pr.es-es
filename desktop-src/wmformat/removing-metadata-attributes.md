---
title: Quitar atributos de metadatos
description: Quitar atributos de metadatos
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows SDK de formato multimedia, quitar atributos de metadatos
- Formato de sistemas avanzados (ASF), quitar atributos de metadatos
- ASF (formato de sistemas avanzados), quitar atributos de metadatos
- metadata,removing attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e09e00fbba8ca5464ccec570a03bbd4e30935238bc531d36ce220a60150839e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110215"
---
# <a name="removing-metadata-attributes"></a>Quitar atributos de metadatos

Puede quitar un atributo de metadatos pasando su índice y número de secuencia al [**método IWMHeaderInfo3::D eleteAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) El orden en el que los atributos restantes se indexa después de quitar un atributo no cambia; todos los atributos restantes que originalmente tenían un valor de índice mayor que el que se quitó tienen sus valores de índice reducidos en uno. Al quitar varios atributos, debe hacerlo en orden descendente por índice para evitar tener que calcular el ajuste en la indexación.

Para mayor comodidad al quitar valores, el método [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) devuelve los valores de índice en orden descendente.

> [!Note]  
> Los valores de índice obtenidos mediante los métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) no son compatibles con los valores de índice obtenidos mediante los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Si usa los métodos de una interfaz para cambiar los atributos de un archivo, debe suponer que los valores de índice recuperados previamente de la otra interfaz ya no son válidos y deben obtenerse de nuevo. Debe evitar el uso de los métodos **de IWMHeaderInfo** si es posible.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




