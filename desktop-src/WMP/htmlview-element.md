---
title: Elemento HTMLView
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento HTMLView especifica la dirección URL base de una página web de HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView Media Player Windows
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699678"
---
# <a name="htmlview-element"></a>Elemento HTMLView

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **HTMLView** especifica la dirección URL base de una página web de HTMLView.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (obligatorio)
</dt> <dd>

Dirección URL base para la Página Web de HTMLView que Windows Media Player muestra.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Puede usar este elemento para integrar la característica HTMLView con la tienda en línea. Si el dominio de la dirección URL especificada por la tienda en línea actual coincide con el de la Página Web de HTMLView, el cambio a **reproducción** en curso se produce sin la intervención del usuario y se muestra el contenido de HTMLView. De lo contrario, Windows Media Player solicita al usuario permiso para mostrar el contenido de HTMLView.

Por ejemplo, si la dirección URL de la Página Web de HTMLView es https://www.proseware.com/html/HTMLView.htm y la dirección URL del atributo **baseurl** se especifica como https://www.proseware.com , se muestra la página web HTMLView sin preguntar al usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





