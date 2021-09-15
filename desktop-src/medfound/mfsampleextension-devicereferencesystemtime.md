---
description: Especifica la marca de tiempo del dispositivo original en el ejemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474066"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>Atributo MFSampleExtension \_ DeviceReferenceSystemTime

Especifica la marca de tiempo del dispositivo original en el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Se trata de una marca de tiempo de referencia de dispositivo de muestras multimedia en resolución de 100ns. Esta marca de tiempo puede llevar o no el valor real del contador de rendimiento de consultas (QPC), en función del origen que produzca las muestras. Otros componentes de la canalización multimedia pueden modificar este valor. Este valor no está disponible para las MTA insertadas en la canalización de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




