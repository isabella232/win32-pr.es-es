---
title: Network.sourceProtocol
description: La propiedad sourceProtocol recupera el protocolo de origen utilizado para recibir datos.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network.sourceProtocol Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967416"
---
# <a name="networksourceprotocol"></a>Network.sourceProtocol

La **propiedad sourceProtocol** recupera el protocolo de origen utilizado para recibir datos.

## <a name="syntax"></a>Sintaxis

*player*. *network*. **sourceProtocol**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Esta propiedad se establece en "" (cadena vacía) al reproducir medios desde un CD o DVD.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **sourceProtocol** para mostrar el protocolo de origen utilizado para recibir datos. La información se muestra en una DIV HTML creada con id. = "SP". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
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
</dt> </dl>

 

 





