---
title: IWMDRMDevice SetLicenseResponse, método
description: El método SetLicenseResponse establece la respuesta de la licencia.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Método SetLicenseResponse de Windows Media Administrador de dispositivos
- Método SetLicenseResponse de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699611"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="b0d71-106">IWMDRMDevice:: SetLicenseResponse (método)</span><span class="sxs-lookup"><span data-stu-id="b0d71-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="b0d71-107">El método **SetLicenseResponse** establece la respuesta de la licencia.</span><span class="sxs-lookup"><span data-stu-id="b0d71-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0d71-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b0d71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0d71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d71-110">*pbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0d71-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d71-111">Especifica la respuesta que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b0d71-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b0d71-112">*cbResponse* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0d71-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d71-113">Tamaño de la respuesta, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b0d71-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d71-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d71-114">Return value</span></span>

<span data-ttu-id="b0d71-115">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b0d71-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b0d71-116">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b0d71-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b0d71-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d71-117">Return code</span></span>                                                                          | <span data-ttu-id="b0d71-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0d71-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b0d71-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d71-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b0d71-120">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="b0d71-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b0d71-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0d71-121">Requirements</span></span>



| <span data-ttu-id="b0d71-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0d71-122">Requirement</span></span> | <span data-ttu-id="b0d71-123">Value</span><span class="sxs-lookup"><span data-stu-id="b0d71-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d71-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0d71-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b0d71-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0d71-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0d71-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0d71-126">Library</span></span><br/> | <dl> <span data-ttu-id="b0d71-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0d71-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d71-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0d71-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d71-129">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="b0d71-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





