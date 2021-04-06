---
title: Mostrando el progreso de la sincronización
description: Mostrando el progreso de la sincronización
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player, dispositivos portátiles
- Modelo de objetos de Windows Media Player, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Control ActiveX de Windows Media Player, dispositivos portátiles
- Control ActiveX, dispositivos portátiles
- Control ActiveX móvil de Windows Media Player, dispositivos portátiles
- Windows Media Player dispositivos móviles y portátiles
- dispositivos portátiles, progreso de sincronización
- sincronización de dispositivos, mostrando el progreso
- sincronizar dispositivos, mostrar el progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904406"
---
# <a name="showing-synchronization-progress"></a><span data-ttu-id="0ad56-113">Mostrando el progreso de la sincronización</span><span class="sxs-lookup"><span data-stu-id="0ad56-113">Showing Synchronization Progress</span></span>

<span data-ttu-id="0ad56-114">Puede mostrar el progreso de la sincronización al usuario.</span><span class="sxs-lookup"><span data-stu-id="0ad56-114">You can display synchronization progress to the user.</span></span> <span data-ttu-id="0ad56-115">En el ejemplo de código siguiente se muestra cómo crear un temporizador para recuperar periódicamente el valor de progreso actual mediante **IWMPSyncDevice:: get \_ Progress**.</span><span class="sxs-lookup"><span data-stu-id="0ad56-115">The following example code shows how to create a timer to periodically retrieve the current progress value by using **IWMPSyncDevice::get\_progress**.</span></span> <span data-ttu-id="0ad56-116">Tenga en cuenta que el valor de progreso recuperado representa el progreso de la operación de sincronización completa de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ad56-116">Note that the progress value retrieved represents the progress for the entire synchronization operation for each device.</span></span> <span data-ttu-id="0ad56-117">No se admite la recuperación del progreso de sincronización de elementos multimedia individuales.</span><span class="sxs-lookup"><span data-stu-id="0ad56-117">Retrieving synchronization progress for individual media items is not supported.</span></span>

<span data-ttu-id="0ad56-118">Para determinar cuándo debe iniciarse o detenerse el temporizador, controle el evento **DeviceSyncStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0ad56-118">To determine when to start or stop the timer, handle the **DeviceSyncStateChange** event.</span></span> <span data-ttu-id="0ad56-119">En la función de ejemplo siguiente se muestra este tipo de controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="0ad56-119">The following example function demonstrates such an event handler.</span></span> <span data-ttu-id="0ad56-120">El código también muestra el estado de sincronización actual como una cadena de texto mediante un control de texto estático, denominado IDC \_ SYNCSTATE.</span><span class="sxs-lookup"><span data-stu-id="0ad56-120">The code also displays the current synchronization state as a text string using a static text control, named IDC\_SYNCSTATE.</span></span>


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



<span data-ttu-id="0ad56-121">Cuando el temporizador se está ejecutando, envía un \_ mensaje del temporizador de WM a intervalos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="0ad56-121">When the timer is running, it sends a WM\_TIMER message at one-second intervals.</span></span> <span data-ttu-id="0ad56-122">La aplicación controla el \_ temporizador de WM en su bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0ad56-122">The application handles WM\_TIMER in its message loop.</span></span>

<span data-ttu-id="0ad56-123">En la función de ejemplo siguiente se muestra cómo mostrar el progreso mediante el uso de un control de texto estático (IDC \_ PROGSTATIC) y el uso de un control de progreso (IDC \_ SYNCPROG).</span><span class="sxs-lookup"><span data-stu-id="0ad56-123">The following example function demonstrates how to show progress by using both a static text control (IDC\_PROGSTATIC), and using a progress control (IDC\_SYNCPROG).</span></span> <span data-ttu-id="0ad56-124">Llame a esta función en respuesta al mensaje del temporizador de WM \_ y al finalizar el proceso de sincronización, como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="0ad56-124">Call this function in response to the WM\_TIMER message and upon completion of the synchronization process, as shown in the preceding example.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0ad56-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ad56-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad56-126">**Enumerar dispositivos**</span><span class="sxs-lookup"><span data-stu-id="0ad56-126">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="0ad56-127">**Interfaz IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="0ad56-127">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="0ad56-128">**IWMPSyncDevice:: get \_ Progress**</span><span class="sxs-lookup"><span data-stu-id="0ad56-128">**IWMPSyncDevice::get\_progress**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[<span data-ttu-id="0ad56-129">**IWMPSyncDevice::isIdentical**</span><span class="sxs-lookup"><span data-stu-id="0ad56-129">**IWMPSyncDevice::isIdentical**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[<span data-ttu-id="0ad56-130">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="0ad56-130">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




