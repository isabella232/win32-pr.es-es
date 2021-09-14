---
title: VIEW.returnToMediaCenter
description: El método returnToMediaCenter devuelve al usuario al modo completo de Reproductor de Windows Media.
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- View.returnToMediaCenter Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070767"
---
# <a name="viewreturntomediacenter"></a>VIEW.returnToMediaCenter

El **método returnToMediaCenter** devuelve al usuario al modo completo de Reproductor de Windows Media.

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> </dl>

 

 





