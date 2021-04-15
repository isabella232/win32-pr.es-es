---
title: Método CreateObject de IWMDRMProvider (wmdrmsdk. h)
description: El método CreateObject recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Método CreateObject formato de Windows Media
- Método CreateObject formato de Windows Media, interfaz IWMDRMProvider
- Interfaz IWMDRMProvider formato de Windows Media, CreateObject (método)
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649579"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="0b0bc-106">IWMDRMProvider:: CreateObject (método)</span><span class="sxs-lookup"><span data-stu-id="0b0bc-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="0b0bc-107">El método **CreateObject** recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b0bc-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="0b0bc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b0bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b0bc-110">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b0bc-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0bc-111">Identificador de la interfaz que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="0b0bc-112">Establezca en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="0b0bc-113">\_IWMDRMLICENSEMANAGEMENT IID</span><span class="sxs-lookup"><span data-stu-id="0b0bc-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="0b0bc-114">\_IWMDRMLICENSEQUERY IID</span><span class="sxs-lookup"><span data-stu-id="0b0bc-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="0b0bc-115">\_IWMDRMNETRECEIVER IID</span><span class="sxs-lookup"><span data-stu-id="0b0bc-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="0b0bc-116">\_IWMDRMNETTRANSMITTER IID</span><span class="sxs-lookup"><span data-stu-id="0b0bc-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="0b0bc-117">\_IWMDRMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="0b0bc-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="0b0bc-118">*ppvObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b0bc-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b0bc-119">Dirección de un puntero que recibe la dirección de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b0bc-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b0bc-120">Return value</span></span>

<span data-ttu-id="0b0bc-121">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b0bc-122">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b0bc-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0b0bc-123">Return code</span></span>                                                                          | <span data-ttu-id="0b0bc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b0bc-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0b0bc-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0b0bc-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0b0bc-126">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b0bc-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b0bc-127">Remarks</span></span>

<span data-ttu-id="0b0bc-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b0bc-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0bc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0bc-129">Requirements</span></span>



| <span data-ttu-id="0b0bc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0bc-130">Requirement</span></span> | <span data-ttu-id="0b0bc-131">Value</span><span class="sxs-lookup"><span data-stu-id="0b0bc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0bc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0bc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0b0bc-133"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0bc-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b0bc-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b0bc-134">Library</span></span><br/> | <dl> <span data-ttu-id="0b0bc-135"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b0bc-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0bc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0bc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0bc-137">**Interfaz IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="0b0bc-138">**Interfaz IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="0b0bc-139">**Interfaz IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="0b0bc-140">**Interfaz IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="0b0bc-141">**Interfaz IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="0b0bc-142">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="0b0bc-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





