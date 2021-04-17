---
title: Función WMDRMCreateProvider (wmdrmsdk. h)
description: La función WMDRMCreateProvider crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Función WMDRMCreateProvider formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718671"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="6e5a7-104">WMDRMCreateProvider función)</span><span class="sxs-lookup"><span data-stu-id="6e5a7-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="6e5a7-105">La función **WMDRMCreateProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="6e5a7-106">Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características DRM protegidas.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5a7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e5a7-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="6e5a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e5a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5a7-109">*ppDRMProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e5a7-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5a7-110">Recibe un puntero a la interfaz [**IWMDRMProvider**](iwmdrmprovider.md) del objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5a7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e5a7-111">Return value</span></span>

<span data-ttu-id="6e5a7-112">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6e5a7-113">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6e5a7-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6e5a7-114">Return code</span></span>                                                                          | <span data-ttu-id="6e5a7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e5a7-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6e5a7-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a7-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6e5a7-117">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="6e5a7-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e5a7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e5a7-118">Requirements</span></span>



| <span data-ttu-id="6e5a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e5a7-119">Requirement</span></span> | <span data-ttu-id="6e5a7-120">Value</span><span class="sxs-lookup"><span data-stu-id="6e5a7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5a7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e5a7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6e5a7-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a7-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e5a7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e5a7-123">Library</span></span><br/> | <dl> <span data-ttu-id="6e5a7-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a7-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e5a7-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e5a7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e5a7-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5a7-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5a7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e5a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5a7-128">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="6e5a7-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="6e5a7-129">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="6e5a7-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





