---
title: Método IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: El método GetSecurityVersion recupera la versión del subsistema DRM en el equipo cliente.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Método GetSecurityVersion formato de Windows Media
- Método GetSecurityVersion formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670741"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="57fd6-106">IWMDRMSecurity:: GetSecurityVersion (método)</span><span class="sxs-lookup"><span data-stu-id="57fd6-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="57fd6-107">El método **GetSecurityVersion** recupera la versión del subsistema DRM en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="57fd6-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fd6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57fd6-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="57fd6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57fd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fd6-110">*pbstrVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57fd6-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57fd6-111">Dirección de una variable que recibe el número de versión del subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="57fd6-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fd6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57fd6-112">Return value</span></span>

<span data-ttu-id="57fd6-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="57fd6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="57fd6-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="57fd6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="57fd6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="57fd6-115">Return code</span></span>                                                                          | <span data-ttu-id="57fd6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="57fd6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="57fd6-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="57fd6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="57fd6-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="57fd6-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57fd6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57fd6-119">Remarks</span></span>

<span data-ttu-id="57fd6-120">El número de versión se expresa como una cadena que consta de cuatro números separados por puntos.</span><span class="sxs-lookup"><span data-stu-id="57fd6-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="57fd6-121">El primer número es el número de versión principal, que normalmente se establece en 2.</span><span class="sxs-lookup"><span data-stu-id="57fd6-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="57fd6-122">El segundo número es el número de versión secundaria, comprendido entre 2 y 10.</span><span class="sxs-lookup"><span data-stu-id="57fd6-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="57fd6-123">El tercer número siempre se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="57fd6-123">The third number is always set to 0.</span></span> <span data-ttu-id="57fd6-124">El cuarto número se establece en 0 o 1, y es un valor booleano que indica si el subsistema se ha individualizado.</span><span class="sxs-lookup"><span data-stu-id="57fd6-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="57fd6-125">Por ejemplo, un número de versión "2.4.0.1" indica la cuarta versión secundaria individual de la segunda versión principal.</span><span class="sxs-lookup"><span data-stu-id="57fd6-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="57fd6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57fd6-126">Requirements</span></span>



| <span data-ttu-id="57fd6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="57fd6-127">Requirement</span></span> | <span data-ttu-id="57fd6-128">Value</span><span class="sxs-lookup"><span data-stu-id="57fd6-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57fd6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57fd6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="57fd6-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fd6-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="57fd6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57fd6-131">Library</span></span><br/> | <dl> <span data-ttu-id="57fd6-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57fd6-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fd6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="57fd6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fd6-134">**Interfaz IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="57fd6-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





