---
title: Elemento Description
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. | Elemento Description
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Descripción, elemento Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4318a7936f4713d3ff89a2fa73731eea0cdd97db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885257"
---
# <a name="description-element"></a>Elemento Description

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento Description** especifica una descripción de marketing de la tienda en línea que se muestra durante la primera experiencia del usuario con una instalación de Reproductor de Windows Media.

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento         |
|-----------------|-----------------|
| Elementos primarios | **ServiceInfo** |
| Elementos secundarios  | Ninguno            |



 

## <a name="remarks"></a>Observaciones

La longitud de la descripción debe ser menor o igual que 255 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------|
| Version<br/> | Reproductor de Windows Media 11.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para un almacén en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





