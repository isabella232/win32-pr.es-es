---
title: Network. lostPackets
description: La propiedad lostPackets recupera el número de paquetes perdidos.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Windows Media Player de red. lostPackets
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
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649844"
---
# <a name="networklostpackets"></a>Network. lostPackets

La propiedad **lostPackets** recupera el número de paquetes perdidos.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **lostPackets**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Esta propiedad solo es válida para streaming multimedia y será igual a cero cuando se use el protocolo HTTP, que es sin pérdida.

Los paquetes se pueden perder por una serie de motivos, como el tipo y la calidad de la conexión de red.

Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero. No se restablece si la reproducción se pausa y se reinicia. Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor*. La propiedad de **dirección URL** está establecida.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **lostPackets** para mostrar el número total de paquetes perdidos durante la reproducción cuando el usuario hace clic en un botón. La información se muestra en un DIV HTML creado con ID = "LP". El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





