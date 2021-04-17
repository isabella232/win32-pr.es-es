---
title: Método IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: El método SetRevocationData establece una lista de revocación de certificados en el almacén local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Método SetRevocationData formato de Windows Media
- Método SetRevocationData formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670567"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="c0a1d-106">IWMDRMSecurity:: SetRevocationData (método)</span><span class="sxs-lookup"><span data-stu-id="c0a1d-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="c0a1d-107">El método **SetRevocationData** establece una lista de revocación de certificados en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a1d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0a1d-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="c0a1d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0a1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a1d-110">*f \_ guidRevocationType* \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a1d-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a1d-111">GUID que especifica el tipo de lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="c0a1d-112">Establezca en una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="c0a1d-113">Constante GUID</span><span class="sxs-lookup"><span data-stu-id="c0a1d-113">GUID constant</span></span>                 | <span data-ttu-id="c0a1d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a1d-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c0a1d-115">\_aplicación REVOCATIONTYPE de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c0a1d-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="c0a1d-116">Especifica la lista de revocación de certificados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="c0a1d-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="c0a1d-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="c0a1d-118">Especifica la lista de revocación de certificados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="c0a1d-119">\_CARDEA REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="c0a1d-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="c0a1d-120">Especifica la lista de revocación de certificados de DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c0a1d-121">*f \_ pbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a1d-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a1d-122">Búfer que contiene la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="c0a1d-123">*f \_ cbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a1d-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a1d-124">Tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a1d-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0a1d-125">Return value</span></span>

<span data-ttu-id="c0a1d-126">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c0a1d-127">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c0a1d-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c0a1d-128">Return code</span></span>                                                                          | <span data-ttu-id="c0a1d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a1d-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c0a1d-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c0a1d-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c0a1d-131">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="c0a1d-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c0a1d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a1d-132">Requirements</span></span>



| <span data-ttu-id="c0a1d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a1d-133">Requirement</span></span> | <span data-ttu-id="c0a1d-134">Value</span><span class="sxs-lookup"><span data-stu-id="c0a1d-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a1d-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0a1d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c0a1d-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a1d-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0a1d-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0a1d-137">Library</span></span><br/> | <dl> <span data-ttu-id="c0a1d-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0a1d-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a1d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0a1d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a1d-140">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="c0a1d-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="c0a1d-141">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="c0a1d-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="c0a1d-142">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="c0a1d-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





