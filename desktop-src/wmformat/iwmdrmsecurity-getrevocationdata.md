---
title: Método IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: El método GetRevocationData recupera una lista de revocación de certificados del almacén local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Método GetRevocationData formato de Windows Media
- Método GetRevocationData formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670569"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="528e5-106">IWMDRMSecurity:: GetRevocationData (método)</span><span class="sxs-lookup"><span data-stu-id="528e5-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="528e5-107">El método **GetRevocationData** recupera una lista de revocación de certificados del almacén local.</span><span class="sxs-lookup"><span data-stu-id="528e5-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="528e5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="528e5-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="528e5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="528e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="528e5-110">*f \_ guidRevocationType* \[\]</span><span class="sxs-lookup"><span data-stu-id="528e5-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="528e5-111">GUID que identifica el tipo de lista de revocación que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="528e5-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="528e5-112">Use una de las constantes de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="528e5-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="528e5-113">Constante GUID</span><span class="sxs-lookup"><span data-stu-id="528e5-113">GUID constant</span></span>                 | <span data-ttu-id="528e5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="528e5-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="528e5-115">\_aplicación REVOCATIONTYPE de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="528e5-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="528e5-116">Especifica la lista de revocación de certificados de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="528e5-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="528e5-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="528e5-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="528e5-118">Especifica la lista de revocación de certificados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="528e5-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="528e5-119">\_CARDEA REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="528e5-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="528e5-120">Especifica la lista de revocación de certificados de DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="528e5-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="528e5-121">*f \_ pbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="528e5-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="528e5-122">Búfer que recibe la lista de revocación.</span><span class="sxs-lookup"><span data-stu-id="528e5-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="528e5-123">Establezca en **null** para obtener el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="528e5-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="528e5-124">*f \_ pcbCRL* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="528e5-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="528e5-125">Tamaño del búfer en bytes.</span><span class="sxs-lookup"><span data-stu-id="528e5-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="528e5-126">Si *f \_ PbCRL* es **null**, este valor se establece en el tamaño de búfer necesario en la salida.</span><span class="sxs-lookup"><span data-stu-id="528e5-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="528e5-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="528e5-127">Return value</span></span>

<span data-ttu-id="528e5-128">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="528e5-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="528e5-129">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="528e5-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="528e5-130">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="528e5-130">Return code</span></span>                                                                          | <span data-ttu-id="528e5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="528e5-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="528e5-132"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="528e5-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="528e5-133">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="528e5-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="528e5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="528e5-134">Requirements</span></span>



| <span data-ttu-id="528e5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="528e5-135">Requirement</span></span> | <span data-ttu-id="528e5-136">Value</span><span class="sxs-lookup"><span data-stu-id="528e5-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="528e5-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="528e5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="528e5-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="528e5-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="528e5-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="528e5-139">Library</span></span><br/> | <dl> <span data-ttu-id="528e5-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="528e5-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="528e5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="528e5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528e5-142">**Revocación y renovación de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="528e5-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="528e5-143">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="528e5-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="528e5-144">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="528e5-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="528e5-145">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="528e5-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





