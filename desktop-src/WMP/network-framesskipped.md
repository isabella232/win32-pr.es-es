---
title: Network.framesSkipped
description: La propiedad framesSkipped recupera el número total de fotogramas omitido durante la reproducción.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network.framesSkipped Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473333"
---
# <a name="networkframesskipped"></a>Network.framesSkipped

La **propiedad framesSkipped** recupera el número total de fotogramas omitido durante la reproducción.

## <a name="syntax"></a>Sintaxis

*player*. *red*. **framesSkipped**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **framesSkipped** para mostrar el número total de fotogramas omitido durante la reproducción cuando el usuario hace clic en un botón. La información se muestra en un DIV HTML creado con id. = "FS". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





