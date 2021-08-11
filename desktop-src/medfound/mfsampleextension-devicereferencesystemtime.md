---
description: Especifica la marca de tiempo del dispositivo original en el ejemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241140"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Atributo MFSampleExtension \_ DeviceReferenceSystemTime

Especifica la marca de tiempo del dispositivo original en el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Se trata de una marca de tiempo de referencia de dispositivo de muestras multimedia en resolución de 100ns. Esta marca de tiempo puede llevar o no el valor real del contador de rendimiento de consultas (QPC), en función del origen que produzca las muestras. Otros componentes de la canalización multimedia pueden modificar este valor. Este valor no está disponible para las MTA insertadas en la canalización de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




