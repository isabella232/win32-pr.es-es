---
title: Network.bufferingCount
description: La propiedad bufferingCount recupera el número de veces que se produjo el almacenamiento en búfer durante la reproducción del clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network.bufferingCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967424"
---
# <a name="networkbufferingcount"></a>Network.bufferingCount

La **propiedad bufferingCount** recupera el número de veces que se produjo el almacenamiento en búfer durante la reproducción del clip.

## <a name="syntax"></a>Sintaxis

*player*. *red*. **bufferingCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

Cada vez que se detiene y reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción está en pausa.

El almacenamiento en búfer solo se aplica al contenido de streaming. Esta propiedad devuelve información válida solo durante el tiempo de ejecución cuando el *reproductor .* Se establece la propiedad **URL.**

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **bufferingCount para** mostrar el número de veces que se produce el almacenamiento en búfer durante la reproducción. La información se muestra en un DIV HTML creado con id. = "CB". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





