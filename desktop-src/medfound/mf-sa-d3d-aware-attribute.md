---
description: Especifica si una transformación Media Foundation (MFT) admite la aceleración de vídeo de DirectX (DXVA). Este atributo solo se aplica a las MFP de vídeo.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: MF_SA_D3D_AWARE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0eaf9ef316e2666f0e962773dcbf25dc5cff17db59f727232b8d502dff83efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876015"
---
# <a name="mf_sa_d3d_aware-attribute"></a>Atributo MF \_ SA \_ D3D \_ AWARE

Especifica si una transformación Media Foundation (MFT) admite la aceleración de vídeo de DirectX (DXVA). Este atributo solo se aplica a las MFP de vídeo.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Para consultar este atributo, llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT. Si **GetAttributes se** realiza correctamente, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Este atributo indica al cliente si MFT puede usar el vídeo de Direct3D 9:

-   Si el atributo es distinto de cero, el cliente puede dar al MFT un puntero a la [**interfaz IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) antes de que se inicie el streaming. Para ello, el cliente envía el [**mensaje MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) al MFT. No es necesario que el cliente envíe este mensaje.
-   Si este atributo es cero **(FALSE),** MFT no admite vídeo de Direct3D 9 y el cliente no debe enviar el mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) al MFT.

El valor predeterminado de este atributo es **FALSE.** Trate este atributo como de solo lectura. No cambie el valor; MFT omitirá los cambios en el valor.

Para obtener más información sobre cómo implementar este atributo en un MFT personalizado, vea [MFT con direct3D.](direct3d-aware-mfts.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="examples"></a>Ejemplos

El código siguiente comprueba si un MFT admite DXVA.


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MTO con direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Compatibilidad con DXVA 2.0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[MODO \_ \_ DXVA DE TOPOLOGÍA \_ MF](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




