---
title: Network.lostPackets
description: La propiedad lostPackets recupera el número de paquetes perdidos.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network.lostPackets Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f4c4211383095559c605de51fd5b182f53632272f268112fd6bdf6aef6dd718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836227"
---
# <a name="networklostpackets"></a>Network.lostPackets

La **propiedad lostPackets** recupera el número de paquetes perdidos.

## <a name="syntax"></a>Syntax

*player*. *red*. **lostPackets**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Esta propiedad solo es válida para los medios de streaming y será igual a cero cuando se use el protocolo HTTP, que no tiene pérdidas.

Los paquetes se pueden perder por diversos motivos, como el tipo y la calidad de la conexión de red.

Cada vez que se detiene y reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción se pausa y se reinicia. Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor .* Se establece la propiedad **URL.**

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **lostPackets para** mostrar el número total de paquetes perdidos durante la reproducción cuando el usuario hace clic en un botón. La información se muestra en un DIV HTML creado con id. = "LP". El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





