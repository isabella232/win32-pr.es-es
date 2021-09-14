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
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073196"
---
# <a name="themecurrentviewid"></a>THEME.currentViewID

El **atributo currentViewID** especifica o recupera la vista mostrada **actualmente.**

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que especifica el **identificador** de la vista **actual.** No tiene valor predeterminado.

## <a name="remarks"></a>Observaciones

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



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> </dl>

 

 





