---
description: El elemento Effect define un objeto de audio o de efecto de vídeo. Se aplica un efecto a un flujo único (como una composición, pista u origen).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653879"
---
# <a name="effect-element"></a>Elemento Effect

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `effect` elemento define un objeto de audio o de efecto de vídeo. Se aplica un efecto a un flujo único (como una composición, pista u origen).

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Parent   | [**compuesto**](composite-element.md), [**agrupar**](group-element.md), [**recortar**](clip-element.md), [**hacer seguimiento**](track-element.md) |
| Children | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Observaciones

El atributo **CLSID** especifica el subobjeto que crea el efecto.

## <a name="examples"></a>Ejemplos


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Gdipluseffects. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




