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
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590325"
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

## <a name="remarks"></a>Comentarios

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Header<br/>                   | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




