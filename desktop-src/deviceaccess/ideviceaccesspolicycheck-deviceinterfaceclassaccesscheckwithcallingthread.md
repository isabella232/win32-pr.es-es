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
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="eef4e-107">IDeviceAccessPolicyCheck::D método eviceInterfaceClassAccessCheckWithCallingThread</span><span class="sxs-lookup"><span data-stu-id="eef4e-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="eef4e-108">Estas interfaces no se admiten y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="eef4e-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="eef4e-109">En su lugar, use las API de la referencia de programación de C++ de la [API de acceso a dispositivos](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="eef4e-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="eef4e-110">Esta API determinará si el token del contexto actual tiene acceso a la clase de interfaz de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="eef4e-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="eef4e-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span><span class="sxs-lookup"><span data-stu-id="eef4e-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef4e-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eef4e-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="eef4e-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eef4e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef4e-114">*pszDeviceInterfaceClassGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eef4e-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-115">GUID de clase de interfaz de dispositivo para el que se debe comprobar el acceso.</span><span class="sxs-lookup"><span data-stu-id="eef4e-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="eef4e-116">*dwClientThreadId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eef4e-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-117">IDENTIFICADOR del subproceso de cliente en el que se debe mostrar cualquier interfaz de usuario asociada si es necesario.</span><span class="sxs-lookup"><span data-stu-id="eef4e-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef4e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eef4e-118">Return value</span></span>

<span data-ttu-id="eef4e-119">Si esta función se ejecuta correctamente, Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="eef4e-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="eef4e-120">De lo contrario, devuelve un código de error HRESULT.</span><span class="sxs-lookup"><span data-stu-id="eef4e-120">Otherwise, it returns an HRESULT error code.</span></span>
