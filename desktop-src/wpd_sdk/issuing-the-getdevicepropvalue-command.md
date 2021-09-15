---
description: Emisión del comando GetDevicePropValue
ms.assetid: 60294ac6-06e0-4546-bbe9-da48d250e31e
title: Emisión del comando GetDevicePropValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d2e5e99e2b1d51b9147fc4da2d86b4fa955907
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466439"
---
# <a name="issuing-the-getdevicepropvalue-command"></a>Emisión del comando GetDevicePropValue

En el ejemplo de esta sección se invoca el **comando MTP GetDevicePropValue** para recuperar la propiedad de dispositivo **BatteryLevel.** (Para obtener una descripción completa de este comando y sus parámetros, vea la [especificación de MTP).](https://www.usb.org/sites/default/files/MTPv1_1.zip)

En el caso de **GetDevicePropValue,** el código de ejemplo usa la secuencia siguiente:

1.  COMANDO WPD \_ \_ MTP EXT EXECUTE COMMAND WITH DATA TO READ (COMANDO MTP EXT EXECUTE DE WPD \_ \_ CON DATOS PARA \_ \_ \_ \_ \_ LEER)
2.  COMANDO WPD \_ \_ MTP \_ EXT READ \_ \_ DATA
3.  TRANSFERENCIA DE DATOS \_ FINALES \_ EXT DEL COMANDO WPD MTP \_ \_ \_ \_

En el ejemplo de código siguiente se muestra cómo la aplicación aplica la secuencia de comandos.


```
#include <portabledevice.h>
#include <portabledeviceapi.h>
#include <wpdmtpextensions.h>

// We'll return the BatteryLevel in the BYREF parameter
HRESULT GetBatteryLevel(IPortableDevice* pDevice, BYTE& bBatteryLevel)
{
    HRESULT hr = S_OK;
    const WORD PTP_OPCODE_GETDEVICEPROPVALUE = 0x1015; 
    const WORD PTP_DEVICEPROPCODE_BATTERYLEVEL = 0x5001; 
    const WORD PTP_RESPONSECODE_OK = 0x2001;     // 0x2001 indicates command success

    // Build basic WPD parameters for the command
    CComPtr<IPortableDeviceValues> spParameters;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**)&spParameters);
    }

    // Use the WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ command here
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                              WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ.pid);
    }

    // Specify the actual MTP opcode to execute here
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_OPERATION_CODE, 
                                                      (ULONG) PTP_OPCODE_GETDEVICEPROPVALUE);
    }

    // GetDevicePropValue requires the property code as an MTP parameter
    // MTP parameters need to be first put into a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spMtpParams;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                                  NULL,
                                  CLSCTX_INPROC_SERVER,
                                  IID_IPortableDevicePropVariantCollection,
                                  (VOID**)&spMtpParams);
    }

    PROPVARIANT pvParam = {0};
    pvParam.vt = VT_UI4;

    // Specify the BatteryLevel property as the MTP parameter
    if (hr == S_OK)
    {
        pvParam.ulVal = PTP_DEVICEPROPCODE_BATTERYLEVEL;
        hr = spMtpParams->Add(&pvParam);
    }

    // Add MTP parameters collection to our main parameter list
    if (hr == S_OK)
    {
        hr = spParameters->SetIPortableDevicePropVariantCollectionValue(
                                          WPD_PROPERTY_MTP_EXT_OPERATION_PARAMS, spMtpParams);
    }  

    // Send the command to initiate the transfer
    CComPtr<IPortableDeviceValues> spResults;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver was able to send the command by interrogating WPD_PROPERTY_COMMON_HRESULT
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (initiating): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the transfer was initiated successfully, the driver returns a context cookie
    LPWSTR pwszCookie = NULL;
    if (hr == S_OK)
    {
         hr = spResults->GetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, &pwszContext);
    }

    // The driver indicates how many bytes will be transferred. This is important to
    // retrieve because we have to read all the data that the device sends us (even if it
    // is not the size we were expecting); otherwise, we run the risk of the device going out of sync
    // with the driver.
    ULONG cbReportedDataSize = 0;
    if (hr == S_OK)
    {
        hr = pResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_TOTAL_DATA_SIZE, 
                                               &cbReportedDataSize);
    }

    // Note: The driver provides an additional property, WPD_PROPERTY_MTP_EXT_OPTIMAL_TRANSFER_BUFFER_SIZE,
    // which suggests the chunk size that the date should be retrieved in. If your application will be 
    // transferring a large amount of data (>256K), use this property to break down the
    // transfer into small chunks so that your app is more responsive.
    // We'll skip this here because device properties are never that big (especially BatteryLevel).
```



En el ejemplo de código siguiente se muestra cómo la aplicación recupera los datos de propiedad.


```
    // If no data will be transferred, skip reading in the data
    BOOL bSkipDataPhase = FALSE;
    if (hr == S_OK && cbReportedDataSize == 0)
    { 
        hr = S_FALSE;
        bSkipDataPhase = TRUE;
    }

    // Use the WPD_COMMAND_MTP_EXT_READ_DATA command to read in the data
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_READ_DATA.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_READ_DATA.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Allocate a buffer for the command to read data into - this should 
    // be the same size as the number of bytes we are expecting to read (per chunk, if applicable).
    BYTE* pbBufferIn = NULL;
    if (hr == S_OK)
    {
        pbBufferIn = (BYTE*) CoTaskMemAlloc(cbReportedDataSize);
        if (pbBufferIn == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Pass the allocated buffer as a parameter
    if (hr == S_OK)
    {
        hr = spParameters->SetBufferValue(WPD_PROPERTY_MTP_EXT_TRANSFER_DATA, 
                                                        pbBufferIn, cbReportedDataSize);
    }

    // Specify the number of bytes to transfer as a parameter
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_TRANSFER_NUM_BYTES_TO_READ, 
                                                        cbReportedDataSize);
    }

    // Send the command to transfer the data
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver was able to transfer the data
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (reading data): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // IMPORTANT: The API does not actually transfer the data into the buffer we provided earlier.
    // Instead, it is available in the results collection.
    BYTE* pbBufferOut = NULL;
    ULONG cbBytesRead = 0;
    if (hr == S_OK)
    {
        hr = pResults->GetBufferValue(WPD_PROPERTY_MTP_EXT_TRANSFER_DATA, &pbBufferOut, &cbBytesRead);
    }

    // Reset hr to S_OK because we skipped the data phase
    if (hr == S_FALSE && bSkipDataPhase == TRUE)
    {
        hr = S_OK;
    }
```



En el ejemplo de código siguiente se muestra cómo la aplicación recupera la respuesta del dispositivo al comando.


```
    // WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER is the command to signal transfer completion
    (void) spParameters->Clear();
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER.pid);
    }

    // Specify the same context that we received earlier
    if (hr == S_OK)
    {
        hr = spParameters->SetStringValue(WPD_PROPERTY_MTP_EXT_TRANSFER_CONTEXT, pwszContext);   
    }

    // Send the completion command
    spResults = NULL;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    }

    // Check if the driver successfully ended the data transfer
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code (ending transfer): 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the command was executed successfully, check the MTP response code to see if the device
    // can handle the command. If the device cannot handle the command, the data phase would 
    // have been skipped (detected by cbReportedDataSize==0) and the MTP response will indicate the
    // error. 
    DWORD dwResponseCode;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_RESPONSE_CODE, &dwResponseCode);
    }

    if (hr == S_OK)
    {
        printf("MTP Response code: 0x%X\n", dwResponseCode);
        hr = (dwResponseCode == (DWORD) PTP_RESPONSECODE_OK) ? S_OK : E_FAIL;
    }

    // If the command was handled by the device, return the property value in the BYREF property
    if (hr == S_OK)
    {
        if (pbBufferOut != NULL)
        {
            bBatteryLevel = (BYTE)(*pbBufferOut);
        }
        else
        {
            // MTP response code was OK, but no data phase occurred
            hr = E_UNEXPECTED;
        }
    }

    // If response parameters are present, they will be contained in the WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS 
    // property. GetDevicePropValue does not return additional response parameters, so skip this code 
    // If required, you might find that code in the post that covered sending MTP commands without data

    // Free up any allocated memory
    CoTaskMemFree(pbBufferIn);
    CoTaskMemFree(pbBufferOut);
    CoTaskMemFree(pwszContext);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



