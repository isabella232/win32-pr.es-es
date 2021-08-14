---
title: THEME.currentViewID
description: El atributo currentViewID especifica o recupera la vista mostrada actualmente.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME.currentViewID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21bf3027b0249286689862e53fc2d616d1d33b19eca562c886e981bffb7f0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117816"
---
# <a name="themecurrentviewid"></a>THEME.currentViewID

El **atributo currentViewID** especifica o recupera la vista mostrada **actualmente.**

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que especifica el **identificador** de la vista **actual.** No tiene valor predeterminado.

## <a name="remarks"></a>Comentarios

Al especificar **currentViewID,** se cierra automáticamente el **objeto currentView** existente (al que apunta el atributo **global** de vista) y se abre el objeto VIEW **especificado.**

## <a name="examples"></a>Ejemplos


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> </dl>

 

 





