---
title: IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread (método)
description: Esta API determinará si el token del contexto actual tiene acceso a la clase de interfaz de dispositivo especificada. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- DeviceInterfaceClassAccessCheckWithCallingThread method Device Access Broker API
- DeviceInterfaceClassAccessCheckWithCallingThread method Device Access Broker API , IDeviceAccessPolicyCheck interface
- IDeviceAccessPolicyCheck interface Device Access Broker API , Método DeviceInterfaceClassAccessCheckWithCallingThread
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f279972c3b716f111fa37fc2dd01ef9184b2f804f07106f6b971358daf290c44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635355"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck::D eviceInterfaceClassAccessCheckWithCallingThread (método)

> [!Important]  
> Estas interfaces no se admiten y no se deben usar. En su lugar, use las API [API de acceso a dispositivos referencia de programación de C++.](device-access-api-c---programming-reference.md)

Esta API determinará si el token del contexto actual tiene acceso a la clase de interfaz de dispositivo especificada. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ En\]
</dt> <dd>

GUID de clase de interfaz de dispositivo para el que se debe comprobar el acceso.

</dd> <dt>

*dwClientThreadId* \[ En\]
</dt> <dd>

Identificador de subproceso de cliente donde se debe mostrar cualquier interfaz de usuario asociada si es necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve S_OK. De lo contrario, devuelve un código de error de HRESULT.
