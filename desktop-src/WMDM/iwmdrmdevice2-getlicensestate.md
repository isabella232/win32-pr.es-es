---
title: IWMDRMDevice2 GetLicenseState, método
description: El método GetLicenseState obtiene el estado de la licencia.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método GetLicenseState de Windows Media Administrador de dispositivos
- Método GetLicenseState de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice2
- Interfaz IWMDRMDevice2 de Windows Media Administrador de dispositivos, método GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700416"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="388ae-106">IWMDRMDevice2:: GetLicenseState (método)</span><span class="sxs-lookup"><span data-stu-id="388ae-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="388ae-107">El método **GetLicenseState** obtiene el estado de la licencia.</span><span class="sxs-lookup"><span data-stu-id="388ae-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="388ae-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="388ae-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="388ae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="388ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="388ae-110">*pbStateQueryData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="388ae-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-111">Puntero a los datos consultados del estado de la licencia.</span><span class="sxs-lookup"><span data-stu-id="388ae-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="388ae-112">*cbStateQueryData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="388ae-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-113">Recuento de los datos consultados.</span><span class="sxs-lookup"><span data-stu-id="388ae-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="388ae-114">*pdwCategory* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="388ae-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-115">Puntero a la categoría.</span><span class="sxs-lookup"><span data-stu-id="388ae-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="388ae-116">*pcRemainingCounts* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="388ae-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-117">Puntero a los recuentos restantes.</span><span class="sxs-lookup"><span data-stu-id="388ae-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="388ae-118">*pcRemainingHours* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="388ae-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-119">Puntero al resto de horas.</span><span class="sxs-lookup"><span data-stu-id="388ae-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="388ae-120">*pdwReserved* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="388ae-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="388ae-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="388ae-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="388ae-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="388ae-122">Return value</span></span>

<span data-ttu-id="388ae-123">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="388ae-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="388ae-124">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="388ae-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="388ae-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="388ae-125">Return code</span></span>                                                                          | <span data-ttu-id="388ae-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="388ae-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="388ae-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="388ae-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="388ae-128">El método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="388ae-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="388ae-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="388ae-129">Requirements</span></span>



| <span data-ttu-id="388ae-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="388ae-130">Requirement</span></span> | <span data-ttu-id="388ae-131">Value</span><span class="sxs-lookup"><span data-stu-id="388ae-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="388ae-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="388ae-132">Header</span></span><br/>  | <dl> <span data-ttu-id="388ae-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="388ae-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="388ae-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="388ae-134">Library</span></span><br/> | <dl> <span data-ttu-id="388ae-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="388ae-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="388ae-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="388ae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388ae-137">**Interfaz IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="388ae-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





