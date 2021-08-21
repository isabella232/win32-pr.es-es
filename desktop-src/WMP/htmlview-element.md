---
title: Elemento HTMLView
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento HTMLView especifica la dirección URL base de una página web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView Reproductor de Windows Media
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 703668427757df19675734e1503296a8a7144517801d0e8fdc0fadb25a16b0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054893"
---
# <a name="htmlview-element"></a>Elemento HTMLView

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento HTMLView** especifica la dirección URL base de una página web HTMLView.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obligatorio)
</dt> <dd>

Dirección URL base de la página web HTMLView que Reproductor de Windows Media muestra.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

Puede usar este elemento para integrar la característica HTMLView con la tienda en línea. Si el dominio de la dirección URL especificada por la tienda en línea actual coincide con el de la página web HTMLView, el cambio a **Reproducción** ahora se produce sin intervención del usuario y se muestra el contenido HTMLView. En caso Reproductor de Windows Media, solicita al usuario permiso para mostrar el contenido HTMLView.

Por ejemplo, si la dirección URL de la página web HTMLView es y la dirección URL del atributo BaseURL se especifica como , la página web HTMLView se muestra sin preguntar https://www.proseware.com/html/HTMLView.htm al  https://www.proseware.com usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





