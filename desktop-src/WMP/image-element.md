---
title: Elemento Image (SDK de WMP)
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento Image (SDK de WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento Image Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9815844833c8068fb89589368f29b15787ad8fb18a21c9f9c6867d202e3095a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862645"
---
# <a name="image-element-wmp-sdk"></a>Elemento Image (SDK de WMP)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento Image** especifica las imágenes que Reproductor de Windows Media muestran al usuario para representar la tienda en línea.

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (necesario para almacenes de tipo 1, omitido para el tipo 2)
</dt> <dd>

Dirección URL del logotipo que Reproductor de Windows Media en el cuadro de diálogo contrato de licencia del usuario final (CLUF). Debe ser una imagen PNG de 80 x 80 píxeles.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (opcional)
</dt> <dd>

Dirección URL de la imagen que Reproductor de Windows Media muestra en el menú servicios. Esta imagen debe ser de 15 x 15 píxeles.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (opcional)
</dt> <dd>

Para una tienda en línea de tipo 1, esta es la dirección URL de la imagen que Reproductor de Windows Media muestra en la **pestaña Tiendas en** línea. Para Reproductor de Windows Media 11, esta imagen debe tener 45 píxeles de ancho por 13 píxeles de alto. Para Reproductor de Windows Media 12, esta imagen debe tener 45 píxeles de ancho por 30 píxeles de alto. Para admitir las versiones 11 y 12 de Reproductor de Windows Media, debe proporcionar dos documentos ServiceInfo.xml independientes, cada uno de los cuales apunta a la imagen de tamaño adecuado para ServiceLargeURL.

Para una tienda en línea de tipo 2, esta es  la dirección URL de la imagen que Reproductor de Windows Media muestra junto a la pestaña Tiendas en línea o junto a los botones del panel de tareas. Esta imagen debe ser de 30 x 30 píxeles.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (opcional)
</dt> <dd>

Dirección URL del logotipo que se muestra junto con la descripción de marketing especificada en el **elemento Description.** Si no se proporciona, estará en blanco. (Todos los tipos, opcional) Debe ser una imagen PNG de 45 píxeles de ancho y 13 píxeles de alto.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos .gif, .jpg, .bmp y .png (que es el formato recomendado). Se admite y se recomienda usar la transparencia web. No se admiten archivos GIF animados.

Si no proporciona un valor para **MenuURL,** Reproductor de Windows Media no muestra ningún gráfico en el menú de la tienda en línea.

Puede proporcionar una imagen animada para ServiceLargeURL. En Reproductor de Windows Media 10 o 11, la imagen se anima. En Reproductor de Windows Media 12, solo se muestra el primer fotograma de la imagen. Para proporcionar una imagen animada, cree un único archivo de imagen que contenga fotogramas sucesivos de la animación. Por ejemplo, para una imagen de 30 píxeles de ancho y 30 píxeles de alto, podría proporcionar 20 imágenes sucesivas en paralelo en una imagen de 600 píxeles de ancho y 30 píxeles de alto. Reproductor de Windows Media animaría automáticamente esta imagen mostrando las 20 imágenes individuales una tras otra. Esta animación se produce solo una vez cuando se abre la tienda en línea; no se repite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





