---
title: IDeviceBroker OpenDeviceFromInterfacePath, método
description: Intenta abrir una instancia de la interfaz de dispositivo en nombre de un cliente. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Método OpenDeviceFromInterfacePath API de agente de acceso a dispositivos
- Método OpenDeviceFromInterfacePath API de agente de acceso a dispositivos, interfaz IDeviceBroker
- Interfaz IDeviceBroker API de agente de acceso de dispositivos, método OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420211"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="516d1-107">IDeviceBroker:: OpenDeviceFromInterfacePath (método)</span><span class="sxs-lookup"><span data-stu-id="516d1-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="516d1-108">Estas interfaces no se admiten y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="516d1-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="516d1-109">En su lugar, use las API de la referencia de programación de C++ de la [API de acceso a dispositivos](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="516d1-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="516d1-110">Intenta abrir una instancia de la interfaz de dispositivo en nombre de un cliente.</span><span class="sxs-lookup"><span data-stu-id="516d1-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="516d1-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span><span class="sxs-lookup"><span data-stu-id="516d1-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="516d1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="516d1-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="516d1-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="516d1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516d1-114">*pszDeviceInterfacePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="516d1-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516d1-115">Instancia de la interfaz de dispositivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="516d1-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="516d1-116">*desiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="516d1-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516d1-117">Acceso deseado que se va a pasar a Open.</span><span class="sxs-lookup"><span data-stu-id="516d1-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="516d1-118">*shareMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="516d1-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516d1-119">Modo de uso compartido que se pasará a Open.</span><span class="sxs-lookup"><span data-stu-id="516d1-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="516d1-120">*flagsAndAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="516d1-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="516d1-121">Marcas y atributos que se van a pasar a Open.</span><span class="sxs-lookup"><span data-stu-id="516d1-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="516d1-122">*\* phDevice* \[\]</span><span class="sxs-lookup"><span data-stu-id="516d1-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="516d1-123">Identificador resultante si se ha abierto correctamente.</span><span class="sxs-lookup"><span data-stu-id="516d1-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516d1-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="516d1-124">Return value</span></span>

<span data-ttu-id="516d1-125">Si esta función se ejecuta correctamente, Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="516d1-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="516d1-126">De lo contrario, devuelve un código de error HRESULT.</span><span class="sxs-lookup"><span data-stu-id="516d1-126">Otherwise, it returns an HRESULT error code.</span></span>
