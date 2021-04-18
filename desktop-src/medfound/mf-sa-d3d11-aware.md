---
description: Especifica si una transformación de Media Foundation (MFT) es compatible con Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360434"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>\_ \_ Atributo compatible con D3D11 de MF SA \_

Especifica si una transformación de Media Foundation (MFT) es compatible con Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo solo se aplica a MFTs de vídeo. Para consultar este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de MFT. Si **GetAttributes** se realiza correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Si el atributo es distinto de cero, el cliente puede dar a la MFT un puntero a la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) antes de que se inicie el streaming. Para ello, el cliente envía el mensaje [**de \_ \_ Administrador de \_ D3D \_ de conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) a la MFT. No es necesario que el cliente envíe este mensaje.
-   Si este atributo es cero (**false**), el MFT no es compatible con Direct3D 11 y el cliente no debe enviar el mensaje de [**Administrador de D3D del \_ conjunto de mensajes \_ \_ \_ MFT**](mft-message-set-d3d-manager.md) a la MFT.

El valor predeterminado de este atributo es **false**. Trate este atributo como de solo lectura. No cambie el valor; la MFT omitirá cualquier cambio en el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




