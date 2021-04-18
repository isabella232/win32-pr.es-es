---
description: Especifica si una transformación de Media Foundation (MFT) es compatible con la aceleración de vídeo de DirectX (DXVA). Este atributo solo se aplica a MFTs de vídeo.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: MF_SA_D3D_AWARE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706643"
---
# <a name="mf_sa_d3d_aware-attribute"></a>\_Atributo MF \_ compatible con D3D de SA \_

Especifica si una transformación de Media Foundation (MFT) es compatible con la aceleración de vídeo de DirectX (DXVA). Este atributo solo se aplica a MFTs de vídeo.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Para consultar este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT. Si **GetAttributes** se realiza correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Este atributo indica al cliente si el MFT puede usar el vídeo de Direct3D 9:

-   Si el atributo es distinto de cero, el cliente puede dar a la MFT un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) antes de que se inicie el streaming. Para ello, el cliente envía el mensaje [**de \_ \_ Administrador de \_ D3D \_ de conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) a la MFT. No es necesario que el cliente envíe este mensaje.
-   Si este atributo es cero (**false**), el MFT no es compatible con el vídeo de Direct3D 9 y el cliente no debe enviar el mensaje de [**Administrador de D3D del \_ conjunto de mensajes \_ \_ \_ MFT**](mft-message-set-d3d-manager.md) a la MFT.

El valor predeterminado de este atributo es **false**. Trate este atributo como de solo lectura. No cambie el valor; la MFT omitirá cualquier cambio en el valor.

Para obtener más información sobre la implementación de este atributo en una MFT personalizada, consulte [MFTs compatible con Direct3D](direct3d-aware-mfts.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="examples"></a>Ejemplos

En el código siguiente se comprueba si una MFT es compatible con DXVA.


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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs compatible con Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Compatibilidad con DXVA 2,0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_ \_ modo DXVA de topología \_ MF](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




