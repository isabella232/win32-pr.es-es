---
title: Network. sourceProtocol
description: La propiedad sourceProtocol recupera el protocolo de origen usado para recibir los datos.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Windows Media Player de red. sourceProtocol
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699480"
---
# <a name="networksourceprotocol"></a>Network. sourceProtocol

La propiedad **sourceProtocol** recupera el protocolo de origen usado para recibir los datos.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **sourceProtocol**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Esta propiedad se establece en "" (cadena vacía) al reproducir archivos multimedia desde un CD o DVD.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **sourceProtocol** para mostrar el protocolo de origen usado para recibir datos. La información se muestra en un DIV HTML creado con ID = "SP". El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





