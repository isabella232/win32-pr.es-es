---
description: Libera los identificadores Plug and Play (PnP) que recuperan los métodos IPortableDeviceManager::GetDevices o IPortableDeviceServiceManager::GetDeviceServices.
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Función FreePortableDevicePnPIDs (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256160"
---
# <a name="freeportabledevicepnpids-function"></a>Función FreePortableDevicePnPIDs

La función auxiliar **FreePortableDevicePnPIDs** libera los identificadores Plug and Play (PnP) que recuperan los métodos [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) o [**IPortableDeviceServiceManager::GetDeviceServices.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)

## <a name="syntax"></a>Sintaxis


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPnPID* 
</dt> <dd>

Matriz de Plug and Play (PnP) que se va a liberar.

</dd> <dt>

*cPnPID* 
</dt> <dd>

Número de identificadores de la matriz especificado por el *parámetro pPnPIDs.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La aplicación es responsable de liberar la matriz de punteros que asigna.

## <a name="examples"></a>Ejemplos


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Encabezado<br/>                   | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




