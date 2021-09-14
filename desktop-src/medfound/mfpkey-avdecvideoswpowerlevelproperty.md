---
description: Especifica el nivel de energía del descodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363842"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>Propiedad MFPKEY \_ AVDecVideoSWPowerLevel

Especifica el nivel de energía del descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

**100**

## <a name="remarks"></a>Observaciones

Esta propiedad debe establecerse en uno de los valores siguientes.



| Value | Significado                                                             |
|-------|---------------------------------------------------------------------|
| 0     | El descodificador usa un nivel de energía optimizado para la duración de la batería.  |
| 50    | El descodificador usa un nivel de energía equilibrado.                            |
| 100   | El descodificador usa un nivel de energía optimizado para la calidad del vídeo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
