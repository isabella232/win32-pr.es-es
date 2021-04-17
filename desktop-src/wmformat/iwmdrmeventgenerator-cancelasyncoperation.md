---
title: Método IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: El método CancelAsyncOperation cancela una operación asincrónica.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Método CancelAsyncOperation formato de Windows Media
- Método CancelAsyncOperation formato de Windows Media, interfaz IWMDRMEventGenerator
- Interfaz IWMDRMEventGenerator formato de Windows Media, método CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660651"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="9963a-106">IWMDRMEventGenerator:: CancelAsyncOperation (método)</span><span class="sxs-lookup"><span data-stu-id="9963a-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="9963a-107">El método **CancelAsyncOperation** cancela una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9963a-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9963a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9963a-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="9963a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9963a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9963a-110">*punkCancelationCookie* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9963a-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9963a-111">Puntero a la cookie de cancelación que identifica la operación asincrónica que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="9963a-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="9963a-112">Esta cookie la proporciona el método que se usa para iniciar la operación.</span><span class="sxs-lookup"><span data-stu-id="9963a-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9963a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9963a-113">Return value</span></span>

<span data-ttu-id="9963a-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9963a-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9963a-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9963a-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9963a-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9963a-116">Return code</span></span>                                                                          | <span data-ttu-id="9963a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9963a-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9963a-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9963a-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9963a-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="9963a-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9963a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9963a-120">Remarks</span></span>

<span data-ttu-id="9963a-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9963a-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="9963a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9963a-122">Requirements</span></span>



| <span data-ttu-id="9963a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9963a-123">Requirement</span></span> | <span data-ttu-id="9963a-124">Value</span><span class="sxs-lookup"><span data-stu-id="9963a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9963a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9963a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9963a-126"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9963a-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="9963a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9963a-127">Library</span></span><br/> | <dl> <span data-ttu-id="9963a-128"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9963a-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9963a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9963a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9963a-130">**Interfaz IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="9963a-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





