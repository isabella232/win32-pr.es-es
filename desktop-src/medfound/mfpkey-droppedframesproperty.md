---
description: Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.
ms.assetid: e55db53e-ab70-42ce-b5cd-2e59a4e96b7b
title: Propiedad MFPKEY_DROPPEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31404218e4e179e19f53e30f5750976c71e0d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812757"
---
# <a name="mfpkey_droppedframes-property"></a>\_Propiedad DROPPEDFRAMES de MFPKEY

Especifica el número de fotogramas de vídeo que se han quitado durante la codificación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

A veces, los fotogramas de vídeo se omiten o se quitan durante la codificación debido a las restricciones de búfer.

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

 

 
