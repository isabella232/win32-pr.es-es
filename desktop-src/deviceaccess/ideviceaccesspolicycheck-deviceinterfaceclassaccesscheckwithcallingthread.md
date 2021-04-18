---
title: IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread, método
description: Esta API determinará si el token del contexto actual tiene acceso a la clase de interfaz de dispositivo especificada. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Método DeviceInterfaceClassAccessCheckWithCallingThread API de agente de acceso a dispositivos
- Método DeviceInterfaceClassAccessCheckWithCallingThread API de agente de acceso a dispositivos, interfaz IDeviceAccessPolicyCheck
- Interfaz IDeviceAccessPolicyCheck API de agente de acceso de dispositivos, método DeviceInterfaceClassAccessCheckWithCallingThread
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
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105720123"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a>IDeviceAccessPolicyCheck::D método eviceInterfaceClassAccessCheckWithCallingThread

> [!Important]  
> Estas interfaces no se admiten y no se deben usar. En su lugar, use las API de la referencia de programación de C++ de la [API de acceso a dispositivos](device-access-api-c---programming-reference.md) .

Esta API determinará si el token del contexto actual tiene acceso a la clase de interfaz de dispositivo especificada. IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDeviceInterfaceClassGuid* \[ de\]
</dt> <dd>

GUID de clase de interfaz de dispositivo para el que se debe comprobar el acceso.

</dd> <dt>

*dwClientThreadId* \[ de\]
</dt> <dd>

IDENTIFICADOR del subproceso de cliente en el que se debe mostrar cualquier interfaz de usuario asociada si es necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, Devuelve S_OK. De lo contrario, devuelve un código de error HRESULT.
