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
# <a name="direct3d-device-manager"></a><span data-ttu-id="b087f-103">Administrador de dispositivos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b087f-103">Direct3D Device Manager</span></span>

<span data-ttu-id="b087f-104">El administrador de dispositivos de Microsoft Direct3D habilita dos o más objetos para compartir el mismo dispositivo de Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b087f-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="b087f-105">Un objeto actúa como el propietario del dispositivo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b087f-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="b087f-106">Para compartir el dispositivo, el propietario del dispositivo crea el administrador de dispositivos de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b087f-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="b087f-107">Otros objetos pueden obtener un puntero al administrador de dispositivos desde el propietario del dispositivo y, a continuación, usar el administrador de dispositivos para obtener un puntero al dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b087f-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="b087f-108">Cualquier objeto que use el dispositivo tiene un bloqueo exclusivo, lo que impide que otros objetos usen el dispositivo al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b087f-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="b087f-109">La Administrador de dispositivos de Direct3D solo es compatible con dispositivos Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b087f-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="b087f-110">No es compatible con dispositivos DXGI.</span><span class="sxs-lookup"><span data-stu-id="b087f-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="b087f-111">Para crear el administrador de dispositivos de Direct3D, llame a [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="b087f-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="b087f-112">Esta función devuelve un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) del administrador de dispositivos, junto con un token de restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="b087f-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="b087f-113">El token de restablecimiento permite al propietario del dispositivo Direct3D establecer (y restablecer) el dispositivo en el administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b087f-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="b087f-114">Para inicializar el administrador de dispositivos, llame a [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="b087f-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="b087f-115">Pase un puntero al dispositivo Direct3D, junto con el token de restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="b087f-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="b087f-116">En el código siguiente se muestra cómo crear e inicializar el administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b087f-116">The following code shows how to create and initialize the device manager.</span></span>


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



<span data-ttu-id="b087f-117">El propietario del dispositivo debe proporcionar a otros objetos un método para obtener un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="b087f-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="b087f-118">El mecanismo estándar consiste en implementar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="b087f-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="b087f-119">El GUID del servicio es el \_ servicio de aceleración de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b087f-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="b087f-120">Para compartir el dispositivo entre varios objetos, cada objeto (incluido el propietario del dispositivo) debe tener acceso al dispositivo a través del administrador de dispositivos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="b087f-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="b087f-121">Llame a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b087f-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="b087f-122">Para usar el dispositivo, llame a [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) y pase el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b087f-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="b087f-123">El método devuelve un puntero a la interfaz **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="b087f-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="b087f-124">Se puede llamar al método en modo de bloqueo o en modo de no bloqueo, dependiendo del valor del parámetro *fBlock* .</span><span class="sxs-lookup"><span data-stu-id="b087f-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="b087f-125">Cuando haya terminado de usar el dispositivo, llame a [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="b087f-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="b087f-126">Este método hace que el dispositivo esté disponible para otros objetos.</span><span class="sxs-lookup"><span data-stu-id="b087f-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="b087f-127">Antes de salir, llame a [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) para cerrar el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b087f-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="b087f-128">Debe mantener el bloqueo del dispositivo solo mientras usa el dispositivo, ya que mantener el bloqueo del dispositivo impide que otros objetos usen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b087f-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="b087f-129">El propietario del dispositivo puede cambiar a otro dispositivo en cualquier momento llamando a [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), normalmente porque se perdió el dispositivo original.</span><span class="sxs-lookup"><span data-stu-id="b087f-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="b087f-130">La pérdida de dispositivos puede producirse por varias razones, como por ejemplo, cambios en la resolución del monitor, acciones de administración de energía, bloqueo y desbloqueo del equipo, etc.</span><span class="sxs-lookup"><span data-stu-id="b087f-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="b087f-131">Para obtener más información, vea la documentación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b087f-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="b087f-132">El método [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida todos los identificadores de dispositivo que se abrieron previamente.</span><span class="sxs-lookup"><span data-stu-id="b087f-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="b087f-133">Cuando un identificador de dispositivo no es válido, el método [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) devuelve **DXVA2 \_ E \_ nuevo \_ \_ dispositivo de vídeo**.</span><span class="sxs-lookup"><span data-stu-id="b087f-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="b087f-134">Si esto ocurre, cierre el identificador y llame de nuevo a [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un nuevo identificador de dispositivo, tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="b087f-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="b087f-135">En el ejemplo siguiente se muestra cómo abrir un identificador de dispositivo y bloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b087f-135">The following example shows how to open a device handle and lock the device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b087f-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b087f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b087f-137">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="b087f-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



