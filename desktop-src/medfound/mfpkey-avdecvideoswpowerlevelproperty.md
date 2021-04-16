---
description: Especifica el nivel de energía para el descodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Propiedad MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696596"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>\_Propiedad AVDecVideoSWPowerLevel de MFPKEY

Especifica el nivel de energía para el descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

**100**

## <a name="remarks"></a>Observaciones

Esta propiedad debe establecerse en uno de los valores siguientes.



| Value | Significado                                                             |
|-------|---------------------------------------------------------------------|
| 0     | El descodificador usa un nivel de energía optimizado para la duración de la batería.  |
| 50    | El descodificador utiliza un nivel de energía equilibrado.                            |
| 100   | El descodificador usa un nivel de energía optimizado para la calidad de vídeo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
