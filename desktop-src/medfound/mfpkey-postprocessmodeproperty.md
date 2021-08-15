---
description: Especifica el modo de procesamiento posterior para el descodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce916d0b74c25ae2a57a43acde128ce8c45e7eb42860c3d7a2f129ea2d5b3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973554"
---
# <a name="mfpkey_postprocessmode-property"></a>Propiedad POSTPROCESSMODE de MFPKEY \_

Especifica el modo de procesamiento posterior para el descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Comentarios

Establezca esta propiedad en uno de los valores siguientes.



| Valor | Significado                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | El descodificador establece el modo de procesamiento posterior de forma adaptable en función de los recursos de CPU disponibles. |
| 0     | El descodificador no realiza ningún procesamiento posterior.                                               |
| 1     | fEl descodificador realiza un desbloqueo rápido.                                                 |
| 2     | El descodificador realiza el desbloqueo completo.                                                  |
| 3     | El descodificador realiza un desbloqueo y una depuración rápidos.                                    |
| 4     | El descodificador realiza el desbloqueo y la desasoción completos.                                    |



 

A medida que el valor de esta propiedad va de 0 a 4, aumenta la complejidad de la decodificación, el uso de recursos de CPU y la calidad de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




