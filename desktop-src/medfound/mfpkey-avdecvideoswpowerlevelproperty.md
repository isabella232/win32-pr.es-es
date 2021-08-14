---
description: Especifica el nivel de energía del descodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874069"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>Propiedad MFPKEY \_ AVDecVideoSWPowerLevel

Especifica el nivel de energía del descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

**100**

## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en uno de los valores siguientes.



| Valor | Significado                                                             |
|-------|---------------------------------------------------------------------|
| 0     | El descodificador usa un nivel de energía optimizado para la duración de la batería.  |
| 50    | El descodificador usa un nivel de energía equilibrado.                            |
| 100   | El descodificador usa un nivel de energía optimizado para la calidad del vídeo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
