---
title: IWMDRMDevice2 GetPartialSyncList, método
description: El método GetPartialSyncList obtiene una lista de sincronización parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList de Windows Media Administrador de dispositivos
- Método GetPartialSyncList de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice2
- Interfaz IWMDRMDevice2 de Windows Media Administrador de dispositivos, método GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700203"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="1c4e9-106">IWMDRMDevice2:: GetPartialSyncList (método)</span><span class="sxs-lookup"><span data-stu-id="1c4e9-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="1c4e9-107">El método **GetPartialSyncList** obtiene una lista de sincronización parcial.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c4e9-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="1c4e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c4e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4e9-110">*cMinCountThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-111">Umbral de recuento mínimo.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-112">*cMinHoursThreshold* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-113">Umbral mínimo de horas.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-114">*dwStartingIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-115">Posición inicial de la indización.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-116">*cItems* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-117">Recuento de elementos que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-118">*ppbSyncList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-119">Lista de sincronización de licencias recuperada.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-120">*pcbSyncList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-121">Tamaño de la lista de sincronización de licencias, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-122">*pdwNextStartingIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-123">Posición inicial siguiente para la indexación.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="1c4e9-124">*pcItemsProcessed* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c4e9-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4e9-125">Recuento de elementos que se están procesando.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4e9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c4e9-126">Return value</span></span>

<span data-ttu-id="1c4e9-127">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1c4e9-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c4e9-128">Todos los métodos de interfaz de Windows Media Administrador de dispositivos pueden devolver cualquiera de las siguientes clases de códigos de error:</span><span class="sxs-lookup"><span data-stu-id="1c4e9-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="1c4e9-129">Códigos de error COM estándar</span><span class="sxs-lookup"><span data-stu-id="1c4e9-129">Standard COM error codes</span></span>
-   <span data-ttu-id="1c4e9-130">Códigos de error de Windows convertidos en valores HRESULT</span><span class="sxs-lookup"><span data-stu-id="1c4e9-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="1c4e9-131">Códigos de error de Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="1c4e9-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="1c4e9-132">Para obtener una lista extensa de posibles códigos de error, consulte [códigos de error](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1c4e9-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4e9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c4e9-133">Requirements</span></span>



| <span data-ttu-id="1c4e9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4e9-134">Requirement</span></span> | <span data-ttu-id="1c4e9-135">Value</span><span class="sxs-lookup"><span data-stu-id="1c4e9-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4e9-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c4e9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1c4e9-137"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c4e9-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="1c4e9-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c4e9-138">Library</span></span><br/> | <dl> <span data-ttu-id="1c4e9-139"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c4e9-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4e9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c4e9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4e9-141">**IWMDRMDevice::GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="1c4e9-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="1c4e9-142">**Interfaz IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="1c4e9-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





