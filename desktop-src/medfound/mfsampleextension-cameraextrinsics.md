---
description: Contiene los elementos extrínsecos de la cámara para el ejemplo.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: MFSampleExtension_CameraExtrinsics atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263196"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a>Atributo MFSampleExtension \_ CameraExtrinsics

Contiene los elementos extrínsecos de la cámara para el ejemplo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

El valor del atributo es [**MFCameraExtrinsics.**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics)

Este atributo es opcional para admitir cámaras que no están calibradas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




