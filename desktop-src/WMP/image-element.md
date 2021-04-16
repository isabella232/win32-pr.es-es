---
title: Elemento Image (SDK de WMP)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento Image (SDK de WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento de imagen Media Player de Windows
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699983"
---
# <a name="image-element-wmp-sdk"></a>Elemento Image (SDK de WMP)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **Image** especifica las imágenes que Windows Media Player muestra al usuario para representar la tienda en línea.

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

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (necesario para los almacenes de tipo 1, omitido para el tipo 2)
</dt> <dd>

Dirección URL del logotipo que Windows Media Player muestra en el cuadro de diálogo contrato de licencia para el usuario final (CLUF). Debe ser una imagen PNG de 80 x 80 píxeles.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (opcional)
</dt> <dd>

Dirección URL de la imagen que Windows Media Player muestra en el menú servicios. Esta imagen debe tener 15 x 15 píxeles.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (opcional)
</dt> <dd>

En el caso de una tienda en línea de tipo 1, se trata de la dirección URL de la imagen que Windows Media Player muestra en la pestaña **tiendas en línea** . En Windows Media Player 11, esta imagen debe tener una anchura de 45 píxeles de ancho por 13 píxeles de alto. En Windows Media Player 12, esta imagen debe tener una anchura de 45 píxeles de ancho por 30 píxeles de alto. Para admitir las versiones 11 y 12 de Windows Media Player, debe proporcionar dos documentos ServiceInfo.xml independientes, cada uno de los cuales señala a la imagen de tamaño adecuado para ServiceLargeURL.

En el caso de una tienda en línea de tipo 2, se trata de la dirección URL de la imagen que Windows Media Player muestra junto a la ficha **tiendas en línea** o junto a los botones del panel de tareas. Esta imagen debe ser 30 x 30 píxeles.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (opcional)
</dt> <dd>

Dirección URL del logotipo que se muestra junto con la descripción de marketing especificada en el elemento **Description** . Si no se proporciona, estará en blanco. (Todos los tipos, opcional) Debe ser una imagen PNG de 45 píxeles de ancho y 13 píxeles de alto.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son. gif,. jpg,. bmp y. png (que es el formato recomendado). El uso de la transparencia web es compatible y recomendado. No se admiten archivos GIF animados.

Si no proporciona un valor para **MenuURL**, Windows Media Player no muestra ningún gráfico en el menú de la tienda en línea.

Puede proporcionar una imagen animada para ServiceLargeURL. En Windows Media Player 10 u 11, la imagen se anima. En Windows Media Player 12, solo se muestra el primer fotograma de la imagen. Para proporcionar una imagen animada, cree un único archivo de imagen que contenga fotogramas sucesivos de la animación. Por ejemplo, para una imagen de 30 píxeles de ancho y 30 píxeles de alto, puede proporcionar 20 imágenes sucesivas en paralelo en una imagen de 600 píxeles de ancho y 30 píxeles de alto. Windows Media Player animaría automáticamente una imagen de este tipo mostrando las 20 imágenes individuales una tras otra. Esta animación se produce una sola vez cuando se abre la tienda en línea; no se repite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





