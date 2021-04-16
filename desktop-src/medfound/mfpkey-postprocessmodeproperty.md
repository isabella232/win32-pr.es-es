---
description: Especifica el modo de procesamiento posterior para el descodificador.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Propiedad MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709234"
---
# <a name="mfpkey_postprocessmode-property"></a>\_Propiedad POSTPROCESSMODE de MFPKEY

Especifica el modo de procesamiento posterior para el descodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Observaciones

Establezca esta propiedad en uno de los siguientes valores.



| Value | Significado                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | El descodificador establece el modo de procesamiento posterior de forma adaptativa en función de los recursos de CPU disponibles. |
| 0     | El descodificador no realiza ningún procesamiento posterior.                                               |
| 1     | el descodificador de la realiza un desbloqueo rápido.                                                 |
| 2     | El descodificador realiza el desbloqueo completo.                                                  |
| 3     | El descodificador realiza un desbloqueo y desanillo rápido.                                    |
| 4     | El descodificador realiza el desbloqueo completo y el desanillo.                                    |



 

Como el valor de esta propiedad va de 0 a 4, se incrementa la complejidad de la descodificación, el uso de recursos de CPU y la calidad de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




