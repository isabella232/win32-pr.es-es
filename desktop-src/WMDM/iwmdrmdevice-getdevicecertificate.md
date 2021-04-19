---
title: IWMDRMDevice GetDeviceCertificate, método
description: El método GetDeviceCertificate recupera el certificado de dispositivo.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Método GetDeviceCertificate de Windows Media Administrador de dispositivos
- Método GetDeviceCertificate de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetDeviceCertificate
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698516"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="75e19-106">IWMDRMDevice:: GetDeviceCertificate (método)</span><span class="sxs-lookup"><span data-stu-id="75e19-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="75e19-107">El método **GetDeviceCertificate** recupera el certificado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75e19-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e19-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75e19-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="75e19-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75e19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e19-110">*pbstrDevCert* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75e19-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75e19-111">Puntero a un **BSTR** que contiene el certificado de dispositivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="75e19-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e19-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75e19-112">Return value</span></span>

<span data-ttu-id="75e19-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="75e19-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75e19-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="75e19-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75e19-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75e19-115">Return code</span></span>                                                                          | <span data-ttu-id="75e19-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="75e19-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="75e19-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="75e19-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="75e19-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="75e19-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75e19-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75e19-119">Requirements</span></span>



| <span data-ttu-id="75e19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="75e19-120">Requirement</span></span> | <span data-ttu-id="75e19-121">Value</span><span class="sxs-lookup"><span data-stu-id="75e19-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e19-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75e19-122">Header</span></span><br/>  | <dl> <span data-ttu-id="75e19-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75e19-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="75e19-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75e19-124">Library</span></span><br/> | <dl> <span data-ttu-id="75e19-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75e19-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e19-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="75e19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e19-127">**Interfaz IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="75e19-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





