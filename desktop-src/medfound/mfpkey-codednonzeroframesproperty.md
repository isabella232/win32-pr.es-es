---
description: Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Propiedad MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716037"
---
# <a name="mfpkey_codednonzeroframes-property"></a>\_Propiedad CODEDNONZEROFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo codificados por el códec que realmente contienen datos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos cualquier fotograma que se haya quitado debido a restricciones de velocidad de bits, menos cualquier trama de cero bytes. Puede obtener este valor después de haber terminado de pasar ejemplos. Los fotogramas de cero bytes se pueden crear para fotogramas duplicados.

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

 

 
