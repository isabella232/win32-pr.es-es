---
description: Contiene los elementos extrínsecos de la cámara para el ejemplo.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: MFSampleExtension_CameraExtrinsics atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109dd0d171468d3a0a3c2c4f06ba1a7edc18707aa1e17afe0d1be65509f4266d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722665"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a>Atributo MFSampleExtension \_ CameraExtrinsics

Contiene los elementos extrínsecos de la cámara para el ejemplo.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**a IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

El valor del atributo es [**MFCameraExtrinsics.**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics)

Este atributo es opcional para admitir cámaras que no están calibradas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




