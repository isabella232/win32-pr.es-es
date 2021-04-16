---
title: IWMDRMDevice IsWMDRMDevice, método
description: El método IsWMDRMDevice determina si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Método IsWMDRMDevice de Windows Media Administrador de dispositivos
- Método IsWMDRMDevice de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699614"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="0d760-106">IWMDRMDevice:: IsWMDRMDevice (método)</span><span class="sxs-lookup"><span data-stu-id="0d760-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="0d760-107">El método **IsWMDRMDevice** determina si el dispositivo admite Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="0d760-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d760-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d760-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="0d760-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d760-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d760-110">*pdwVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d760-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d760-111">Versión de Windows Media DRM 10 para dispositivos portátiles, que tiene el valor 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="0d760-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d760-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d760-112">Return value</span></span>

<span data-ttu-id="0d760-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0d760-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0d760-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0d760-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0d760-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0d760-115">Return code</span></span>                                                                          | <span data-ttu-id="0d760-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d760-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0d760-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d760-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0d760-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0d760-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d760-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d760-119">Requirements</span></span>



| <span data-ttu-id="0d760-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d760-120">Requirement</span></span> | <span data-ttu-id="0d760-121">Value</span><span class="sxs-lookup"><span data-stu-id="0d760-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d760-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d760-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0d760-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d760-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d760-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d760-124">Library</span></span><br/> | <dl> <span data-ttu-id="0d760-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d760-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d760-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d760-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d760-127">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="0d760-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





