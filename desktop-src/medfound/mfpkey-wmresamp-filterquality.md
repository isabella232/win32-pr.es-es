---
description: Especifica la calidad de la salida.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Propiedad MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275847"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>\_ \_ Propiedad FILTERQUALITY de MFPKEY WMRESAMP

Especifica la calidad de la salida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de remuestreador de audio](audioresampler.md)

## <a name="remarks"></a>Observaciones

El intervalo válido de esta propiedad es de 1 a 60, ambos inclusive. Los valores más altos producen una salida de mayor calidad, pero introducen más latencia. Un valor de 1 es esencialmente el mismo que el de la interpolación lineal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
