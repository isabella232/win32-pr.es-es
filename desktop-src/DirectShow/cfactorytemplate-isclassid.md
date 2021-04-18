---
description: El método IsClassID determina si un CLSID coincide con esta plantilla de clase.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Método CFactoryTemplate. IsClassID (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660854"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="41b3a-103">CFactoryTemplate. IsClassID, método</span><span class="sxs-lookup"><span data-stu-id="41b3a-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="41b3a-104">El `IsClassID` método determina si un CLSID coincide con esta plantilla de clase.</span><span class="sxs-lookup"><span data-stu-id="41b3a-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41b3a-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="41b3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b3a-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="41b3a-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="41b3a-108">Referencia a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="41b3a-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b3a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41b3a-109">Return value</span></span>

<span data-ttu-id="41b3a-110">Devuelve **true** si el *parámetro rclsid* es el mismo CLSID que la variable miembro [**CFactoryTemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) ; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="41b3a-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b3a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41b3a-111">Requirements</span></span>



| <span data-ttu-id="41b3a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="41b3a-112">Requirement</span></span> | <span data-ttu-id="41b3a-113">Value</span><span class="sxs-lookup"><span data-stu-id="41b3a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b3a-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41b3a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="41b3a-115"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41b3a-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="41b3a-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41b3a-116">Library</span></span><br/> | <dl> <span data-ttu-id="41b3a-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="41b3a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b3a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="41b3a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b3a-119">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="41b3a-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




