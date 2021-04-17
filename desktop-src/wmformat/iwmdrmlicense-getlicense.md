---
title: Método IWMDRMLicense GetLicense (wmdrmsdk. h)
description: El método GetLicense recupera la licencia como datos XML o XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Método GetLicense formato de Windows Media
- Método GetLicense formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708893"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="32430-106">IWMDRMLicense:: GetLicense (método)</span><span class="sxs-lookup"><span data-stu-id="32430-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="32430-107">El método **GetLicense** recupera la licencia como datos XML o XMR.</span><span class="sxs-lookup"><span data-stu-id="32430-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="32430-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32430-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="32430-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32430-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32430-110">*ppbLicense* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32430-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32430-111">Recibe la licencia.</span><span class="sxs-lookup"><span data-stu-id="32430-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="32430-112">*pcbLicense* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32430-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32430-113">Recibe el tamaño de la licencia.</span><span class="sxs-lookup"><span data-stu-id="32430-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="32430-114">*pdwLicenseType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="32430-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32430-115">Recibe el tipo de la licencia devuelta.</span><span class="sxs-lookup"><span data-stu-id="32430-115">Receives the type of the license returned.</span></span> <span data-ttu-id="32430-116">Este valor se establece en una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="32430-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="32430-117">Constante</span><span class="sxs-lookup"><span data-stu-id="32430-117">Constant</span></span>                  | <span data-ttu-id="32430-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="32430-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="32430-119">tipo de licencia de WMDRM \_ \_ \_ XML</span><span class="sxs-lookup"><span data-stu-id="32430-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="32430-120">La licencia recuperada tiene el formato XML.</span><span class="sxs-lookup"><span data-stu-id="32430-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="32430-121">tipo de licencia de WMDRM \_ \_ \_ XMR</span><span class="sxs-lookup"><span data-stu-id="32430-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="32430-122">La licencia recuperada tiene el formato XMR.</span><span class="sxs-lookup"><span data-stu-id="32430-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32430-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32430-123">Return value</span></span>

<span data-ttu-id="32430-124">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="32430-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="32430-125">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="32430-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="32430-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="32430-126">Return code</span></span>                                                                          | <span data-ttu-id="32430-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="32430-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="32430-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="32430-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32430-129">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="32430-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32430-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32430-130">Remarks</span></span>

<span data-ttu-id="32430-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="32430-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="32430-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32430-132">Requirements</span></span>



| <span data-ttu-id="32430-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="32430-133">Requirement</span></span> | <span data-ttu-id="32430-134">Value</span><span class="sxs-lookup"><span data-stu-id="32430-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32430-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32430-135">Header</span></span><br/>  | <dl> <span data-ttu-id="32430-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="32430-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="32430-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32430-137">Library</span></span><br/> | <dl> <span data-ttu-id="32430-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32430-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32430-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="32430-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32430-140">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="32430-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="32430-141">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="32430-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





