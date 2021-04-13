---
description: Administrador de dispositivos de Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Administrador de dispositivos de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360100"
---
# <a name="direct3d-device-manager"></a>Administrador de dispositivos de Direct3D

El administrador de dispositivos de Microsoft Direct3D habilita dos o más objetos para compartir el mismo dispositivo de Microsoft Direct3D 9. Un objeto actúa como el propietario del dispositivo Direct3D 9. Para compartir el dispositivo, el propietario del dispositivo crea el administrador de dispositivos de Direct3D. Otros objetos pueden obtener un puntero al administrador de dispositivos desde el propietario del dispositivo y, a continuación, usar el administrador de dispositivos para obtener un puntero al dispositivo Direct3D. Cualquier objeto que use el dispositivo tiene un bloqueo exclusivo, lo que impide que otros objetos usen el dispositivo al mismo tiempo.

> [!Note]  
> La Administrador de dispositivos de Direct3D solo es compatible con dispositivos Direct3D 9. No es compatible con dispositivos DXGI.

 

Para crear el administrador de dispositivos de Direct3D, llame a [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Esta función devuelve un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) del administrador de dispositivos, junto con un token de restablecimiento. El token de restablecimiento permite al propietario del dispositivo Direct3D establecer (y restablecer) el dispositivo en el administrador de dispositivos. Para inicializar el administrador de dispositivos, llame a [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Pase un puntero al dispositivo Direct3D, junto con el token de restablecimiento.

En el código siguiente se muestra cómo crear e inicializar el administrador de dispositivos.


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



El propietario del dispositivo debe proporcionar a otros objetos un método para obtener un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . El mecanismo estándar consiste en implementar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . El GUID del servicio es el \_ servicio de aceleración de vídeo Mr \_ \_ .

Para compartir el dispositivo entre varios objetos, cada objeto (incluido el propietario del dispositivo) debe tener acceso al dispositivo a través del administrador de dispositivos, como se indica a continuación:

1.  Llame a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo.
2.  Para usar el dispositivo, llame a [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) y pase el identificador del dispositivo. El método devuelve un puntero a la interfaz **IDirect3DDevice9** . Se puede llamar al método en modo de bloqueo o en modo de no bloqueo, dependiendo del valor del parámetro *fBlock* .
3.  Cuando haya terminado de usar el dispositivo, llame a [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Este método hace que el dispositivo esté disponible para otros objetos.
4.  Antes de salir, llame a [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) para cerrar el identificador del dispositivo.

Debe mantener el bloqueo del dispositivo solo mientras usa el dispositivo, ya que mantener el bloqueo del dispositivo impide que otros objetos usen el dispositivo.

El propietario del dispositivo puede cambiar a otro dispositivo en cualquier momento llamando a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), normalmente porque se perdió el dispositivo original. La pérdida de dispositivos puede producirse por varias razones, como por ejemplo, cambios en la resolución del monitor, acciones de administración de energía, bloqueo y desbloqueo del equipo, etc. Para obtener más información, vea la documentación de Direct3D.

El método [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida todos los identificadores de dispositivo que se abrieron previamente. Cuando un identificador de dispositivo no es válido, el método [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelve **DXVA2 \_ E \_ nuevo \_ \_ dispositivo de vídeo**. Si esto ocurre, cierre el identificador y llame de nuevo a [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un nuevo identificador de dispositivo, tal como se muestra en el código siguiente.

En el ejemplo siguiente se muestra cómo abrir un identificador de dispositivo y bloquear el dispositivo.


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

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



