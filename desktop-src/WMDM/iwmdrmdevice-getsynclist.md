---
title: IWMDRMDevice GetSyncList, método
description: El método GetSyncList recupera la lista de sincronización de licencias en el dispositivo. La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo de acuerdo con los criterios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Método GetSyncList de Windows Media Administrador de dispositivos
- Método GetSyncList de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699615"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="940ad-107">IWMDRMDevice:: GetSyncList (método)</span><span class="sxs-lookup"><span data-stu-id="940ad-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="940ad-108">El método **GetSyncList** recupera la lista de sincronización de licencias en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="940ad-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="940ad-109">La sincronización de licencias permite al equipo host transferir licencias actualizadas a un dispositivo de acuerdo con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="940ad-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="940ad-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="940ad-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="940ad-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="940ad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940ad-112">*cMinCountThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="940ad-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940ad-113">Umbral de recuento mínimo.</span><span class="sxs-lookup"><span data-stu-id="940ad-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="940ad-114">*cMinHoursThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="940ad-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940ad-115">Umbral mínimo de horas.</span><span class="sxs-lookup"><span data-stu-id="940ad-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="940ad-116">*ppbSyncList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="940ad-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940ad-117">Lista de sincronización de licencias recuperada.</span><span class="sxs-lookup"><span data-stu-id="940ad-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="940ad-118">*pcbSyncList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="940ad-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="940ad-119">Tamaño de la lista de sincronización de licencias, en bytes.</span><span class="sxs-lookup"><span data-stu-id="940ad-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940ad-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="940ad-120">Return value</span></span>

<span data-ttu-id="940ad-121">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="940ad-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="940ad-122">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="940ad-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="940ad-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="940ad-123">Return code</span></span>                                                                          | <span data-ttu-id="940ad-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="940ad-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="940ad-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="940ad-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="940ad-126">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="940ad-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="940ad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="940ad-127">Requirements</span></span>



| <span data-ttu-id="940ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="940ad-128">Requirement</span></span> | <span data-ttu-id="940ad-129">Value</span><span class="sxs-lookup"><span data-stu-id="940ad-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="940ad-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="940ad-130">Header</span></span><br/>  | <dl> <span data-ttu-id="940ad-131"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="940ad-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="940ad-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="940ad-132">Library</span></span><br/> | <dl> <span data-ttu-id="940ad-133"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="940ad-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940ad-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="940ad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940ad-135">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="940ad-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





