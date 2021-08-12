---
title: Elemento Color
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Color Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8576f94c2d1aa88608f8f40cbfe32c2d1dc315e0e4578ca6554fa5fcde82c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580760"
---
# <a name="color-element"></a>Elemento Color

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento Color especifica el color de fondo para los botones de navegación de la tienda en línea, el texto de los botones y la barra de tareas Características.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obligatorio)
</dt> <dd>

Valor de color RGB hexadecimal. Especifica el color de fondo de los botones y la barra de tareas.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obligatorio)
</dt> <dd>

Valor de color RGB hexadecimal. Especifica el color del texto del botón.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

El valor predeterminado de **MediaPlayer** es \# 7C9AD6. El valor predeterminado de **MediaPlayerText** es \# FFFFFF.

Asegúrese de usar colores que hagan que sea fácil para el usuario leer el texto del botón. Por ejemplo, debe evitar el uso de texto de botón en blanco en botones de color claro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





