---
description: Direct3D Administrador de dispositivos
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Direct3D Administrador de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2031e336fafd7b98fb02d23fea84c36d27d0f4d3093f0d20991fb8777d6434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064199"
---
# <a name="direct3d-device-manager"></a>Direct3D Administrador de dispositivos

El administrador de dispositivos de Microsoft Direct3D permite que dos o más objetos compartan el mismo dispositivo Microsoft Direct3D 9. Un objeto actúa como propietario del dispositivo Direct3D 9. Para compartir el dispositivo, el propietario del dispositivo crea el administrador de dispositivos Direct3D. Otros objetos pueden obtener un puntero al administrador de dispositivos del propietario del dispositivo y, a continuación, usar el administrador de dispositivos para obtener un puntero al dispositivo Direct3D. Cualquier objeto que use el dispositivo contiene un bloqueo exclusivo, lo que impide que otros objetos utilicen el dispositivo al mismo tiempo.

> [!Note]  
> Direct3D Administrador de dispositivos solo admite dispositivos Direct3D 9. No admite dispositivos DXGI.

 

Para crear el administrador de dispositivos Direct3D, llame a [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Esta función devuelve un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) del administrador de dispositivos, junto con un token de restablecimiento. El token de restablecimiento permite al propietario del dispositivo Direct3D establecer (y restablecer) el dispositivo en el administrador de dispositivos. Para inicializar el administrador de dispositivos, llame a [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Pase un puntero al dispositivo Direct3D, junto con el token de restablecimiento.

El código siguiente muestra cómo crear e inicializar el administrador de dispositivos.


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



El propietario del dispositivo debe proporcionar una manera de que otros objetos obtengan un puntero a la [**interfaz IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) El mecanismo estándar es implementar la [**interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) El GUID del servicio es MR \_ VIDEO \_ ACCELERATION \_ SERVICE.

Para compartir el dispositivo entre varios objetos, cada objeto (incluido el propietario del dispositivo) debe acceder al dispositivo a través del administrador de dispositivos, como se muestra a continuación:

1.  Llame [**a IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo.
2.  Para usar el dispositivo, llame a [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) y pase el identificador del dispositivo. El método devuelve un puntero a la **interfaz IDirect3DDevice9.** Se puede llamar al método en un modo de bloqueo o en un modo sin bloqueo, dependiendo del valor del *parámetro fBlock.*
3.  Cuando haya terminado de usar el dispositivo, llame a [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Este método hace que el dispositivo esté disponible para otros objetos.
4.  Antes de salir, llame a [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) para cerrar el identificador del dispositivo.

Debe mantener el bloqueo del dispositivo solo mientras usa el dispositivo, ya que mantener el bloqueo del dispositivo impide que otros objetos utilicen el dispositivo.

El propietario del dispositivo puede cambiar a otro dispositivo en cualquier momento llamando a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), normalmente porque se perdió el dispositivo original. La pérdida de dispositivos puede producirse por diversos motivos, como cambios en la resolución del monitor, acciones de administración de energía, bloqueo y desbloqueo del equipo, etc. Para más información, consulte la documentación de Direct3D.

El [**método ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida los identificadores de dispositivo que se abrieron anteriormente. Cuando un identificador de dispositivo no es válido, [**el método LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelve **DXVA2 \_ E NEW VIDEO \_ \_ \_ DEVICE**. Si esto ocurre, cierre el identificador y vuelva a llamar a [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un nuevo identificador de dispositivo, como se muestra en el código siguiente.

En el ejemplo siguiente se muestra cómo abrir un identificador de dispositivo y bloquearlo.


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



