---
title: Mostrar el progreso de la sincronización
description: Mostrar el progreso de la sincronización
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Reproductor de Windows Media dispositivos portátiles
- Reproductor de Windows Media de objetos, dispositivos portátiles
- modelo de objetos, dispositivos portátiles
- Reproductor de Windows Media ActiveX, dispositivos portátiles
- ActiveX, dispositivos portátiles
- Reproductor de Windows Media Control ActiveX dispositivos móviles, dispositivos portátiles
- Reproductor de Windows Media Dispositivos móviles y portátiles
- dispositivos portátiles, progreso de sincronización
- sincronización de dispositivos, que muestra el progreso
- sincronizar dispositivos, mostrar el progreso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126bff5f96aa9b18c1729d0da12b05a73da6eb43dd63d8135baf0544e19ada5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833296"
---
# <a name="showing-synchronization-progress"></a>Mostrar el progreso de la sincronización

Puede mostrar el progreso de la sincronización al usuario. El código de ejemplo siguiente muestra cómo crear un temporizador para recuperar periódicamente el valor de progreso actual mediante **IWMPSyncDevice::get \_ progress**. Tenga en cuenta que el valor de progreso recuperado representa el progreso de toda la operación de sincronización para cada dispositivo. No se admite la recuperación del progreso de sincronización de elementos multimedia individuales.

Para determinar cuándo iniciar o detener el temporizador, controle el **evento DeviceSyncStateChange.** La siguiente función de ejemplo muestra este tipo de controlador de eventos. El código también muestra el estado de sincronización actual como una cadena de texto mediante un control de texto estático, denominado IDC \_ SYNCSTATE.


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



Cuando se ejecuta el temporizador, envía un mensaje WM TIMER a \_ intervalos de un segundo. La aplicación controla WM \_ TIMER en su bucle de mensajes.

En la siguiente función de ejemplo se muestra cómo mostrar el progreso mediante un control de texto estático (IDC PROGSTATIC) y un control de progreso \_ (IDC \_ SYNCPROG). Llame a esta función en respuesta al mensaje WM TIMER y tras la finalización del proceso de \_ sincronización, como se muestra en el ejemplo anterior.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Enumeración de dispositivos**](enumerating-devices.md)
</dt> <dt>

[**IWMPSyncDevice (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ progress**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**IWMPSyncDevice::isIdentical**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




