---
description: Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1263a15d9ddd678360bf57f5f704143d580d6b17ab63af0777c20d9b09204cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954685"
---
# <a name="mfpkey_codednonzeroframes-property"></a>Propiedad \_ CODEDNONZEROFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos los fotogramas que se descartaron debido a restricciones de velocidad de bits, menos los fotogramas de cero bytes. Puede obtener este valor una vez que haya terminado de pasar ejemplos. Se pueden crear fotogramas de cero bytes para fotogramas duplicados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
