---
title: Network. maxBandwidth
description: La propiedad maxBandwidth especifica o recupera el ancho de banda máximo permitido.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Red. maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649494"
---
# <a name="networkmaxbandwidth"></a>Network. maxBandwidth

La propiedad **maxBandwidth** especifica o recupera el ancho de banda máximo permitido.

## <a name="syntax"></a>Sintaxis

*reproductor*. *red*. **maxBandwidth**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**).

## <a name="remarks"></a>Observaciones

Esta propiedad no tiene ningún valor predeterminado. Se puede especificar su valor mientras se reproduce Windows Media Player, pero el cambio no surtirá efecto hasta que se libere el elemento multimedia actual abriendo otro o llamando al *reproductor*. **cierre**. Windows Media Player intenta lograr el ancho de banda más alto posible. Solo en el caso del valor que se está configurando, se producirá cualquier reducción del ancho de banda.

Esta configuración es útil para reducir la cantidad de ancho de banda que se usa, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR). Una secuencia MBR contiene varias secuencias con velocidades de bits diferentes. En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits menor que la que requiere el cliente. En este caso, si se establece la propiedad **maxBandwidth** , se seleccionará una secuencia de velocidad de bits inferior.

Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (kbps), 37 Kbps y 200 Kbps. Si se establece la propiedad **maxBandwidth** en 50.000 (50 Kbps), se seleccionará la secuencia de 37 kbps en lugar de la secuencia de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





