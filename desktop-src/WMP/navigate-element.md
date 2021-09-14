---
title: Elemento Navigate
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento Navigate especifica una dirección URL utilizada por las llamadas a External.NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Elemento Navigate Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967464"
---
# <a name="navigate-element"></a>Elemento Navigate

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento Navigate** especifica una dirección URL utilizada por las llamadas a **External.NavigateTaskPaneURL.**

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                                             | Descripción                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obligatorio)<br/> | Dirección URL completa de la página web a la que se va a navegar. **NavigateTaskPaneURL puede** anexar una cadena de consulta a esta dirección URL.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





