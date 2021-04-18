---
description: Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Propiedad MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276307"
---
# <a name="mfpkey_producedummyframes-property"></a>\_Propiedad PRODUCEDUMMYFRAMES de MFPKEY

Especifica si el codificador genera entradas de fotogramas ficticias en el flujo de bits para los fotogramas duplicados.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCProduceDummyFrames

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ false

## <a name="remarks"></a>Observaciones

Si este valor es VARIANT \_ false, el códec no colocará ningún dato en el flujo de bits para los fotogramas duplicados.

Los marcos ficticios pueden ser importantes en las aplicaciones donde se conservan los números de fotogramas. Un ejemplo común es cuando se mantienen códigos de tiempo SMPTE para contenido codificado.

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

 

 




