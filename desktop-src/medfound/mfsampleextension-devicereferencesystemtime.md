---
description: Especifica la marca de tiempo del dispositivo original en el ejemplo.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908379"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>\_Atributo DeviceReferenceSystemTime de MFSampleExtension

Especifica la marca de tiempo del dispositivo original en el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Se trata de una marca de tiempo de referencia de dispositivo de ejemplos de medios en la resolución de 100 NS. Esta marca de tiempo puede o no contener el valor real del contador de rendimiento de la consulta (QPC), dependiendo del origen que produzca los ejemplos. Otros componentes de la canalización multimedia pueden modificar este valor. Este valor no está disponible para MFTs insertado en la canalización de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




