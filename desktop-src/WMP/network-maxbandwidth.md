---
title: Network.maxBandwidth
description: La propiedad maxBandwidth especifica o recupera el ancho de banda máximo permitido.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Network.maxBandwidth Reproductor de Windows Media
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
ms.openlocfilehash: 15c06c84762cd0d68af8af1cc9405036c5aecce317a61dbf292d3213bed351e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574151"
---
# <a name="networkmaxbandwidth"></a>Network.maxBandwidth

La **propiedad maxBandwidth** especifica o recupera el ancho de banda máximo permitido.

## <a name="syntax"></a>Syntax

*player*. *network*. **maxBandwidth**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** (**long**).

## <a name="remarks"></a>Comentarios

Esta propiedad no tiene ningún valor predeterminado. Su valor se puede especificar mientras Reproductor de Windows Media está reproduciendo, pero el cambio no tendrá efecto hasta que se libera el elemento multimedia actual abriendo otro o llamando al *Reproductor*. **cierre**. Reproductor de Windows Media intentos de lograr el mayor ancho de banda posible. Solo en el caso del valor que se establece se producirá una reducción del ancho de banda.

Esta configuración es útil para reducir la cantidad de ancho de banda usado, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR). Una secuencia MBR contiene varias secuencias con velocidades de bits diferentes. En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits inferior a la que requiere el cliente. En este caso, al establecer **la propiedad maxBandwidth** se seleccionará una secuencia de velocidad de bits inferior.

Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (Kbps), 37 Kbps y 200 Kbps. Al establecer la propiedad **maxBandwidth** en 50 000 (50 Kbps), se seleccionará la secuencia de 37 Kbps en lugar de la secuencia de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Player.close**](player-close.md)
</dt> </dl>

 

 





