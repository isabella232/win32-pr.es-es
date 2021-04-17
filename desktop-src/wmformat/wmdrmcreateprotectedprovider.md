---
title: Función WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: La función WMDRMCreateProtectedProvider crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Función WMDRMCreateProtectedProvider formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698648"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="28004-104">WMDRMCreateProtectedProvider función)</span><span class="sxs-lookup"><span data-stu-id="28004-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="28004-105">La función **WMDRMCreateProtectedProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="28004-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="28004-106">Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características DRM protegidas.</span><span class="sxs-lookup"><span data-stu-id="28004-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="28004-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28004-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="28004-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28004-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28004-109">*ppDRMProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28004-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28004-110">Recibe un puntero a la interfaz [**IWMDRMProvider**](iwmdrmprovider.md) del objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="28004-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28004-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28004-111">Return value</span></span>

<span data-ttu-id="28004-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="28004-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="28004-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="28004-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="28004-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="28004-114">Return code</span></span>                                                                          | <span data-ttu-id="28004-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="28004-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="28004-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="28004-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="28004-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="28004-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28004-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28004-118">Remarks</span></span>

<span data-ttu-id="28004-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28004-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="28004-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28004-120">Requirements</span></span>



| <span data-ttu-id="28004-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28004-121">Requirement</span></span> | <span data-ttu-id="28004-122">Value</span><span class="sxs-lookup"><span data-stu-id="28004-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28004-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28004-123">Header</span></span><br/> | <dl> <span data-ttu-id="28004-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="28004-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28004-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="28004-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28004-126">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="28004-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="28004-127">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="28004-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





