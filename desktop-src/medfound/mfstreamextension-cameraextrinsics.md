---
description: Contiene la cámara extrinsics para la secuencia.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: MFStreamExtension_CameraExtrinsics atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155364"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a>\_Atributo CameraExtrinsics de MFStreamExtension

Contiene la cámara extrinsics para la secuencia.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).

## <a name="remarks"></a>Observaciones

El valor del atributo es [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




