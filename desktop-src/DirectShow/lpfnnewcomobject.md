---
description: 'Puntero de función LPFNNewCOMObject: puntero a una función que crea una instancia del objeto .'
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntero de función LPFNNewCOMObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116533"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="cd0c9-103">Puntero de función LPFNNewCOMObject</span><span class="sxs-lookup"><span data-stu-id="cd0c9-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="cd0c9-104">Puntero a una función que crea una instancia del objeto .</span><span class="sxs-lookup"><span data-stu-id="cd0c9-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd0c9-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="cd0c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd0c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd0c9-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="cd0c9-108">Puntero a **la interfaz IUnknown** del objeto que agrega el nuevo objeto, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="cd0c9-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="cd0c9-109">Este puntero puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="cd0c9-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd0c9-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cd0c9-111">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="cd0c9-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="cd0c9-112">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="cd0c9-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd0c9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd0c9-113">Return value</span></span>

<span data-ttu-id="cd0c9-114">Devuelve un puntero a una nueva instancia del objeto .</span><span class="sxs-lookup"><span data-stu-id="cd0c9-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd0c9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd0c9-115">Requirements</span></span>



| <span data-ttu-id="cd0c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd0c9-116">Requirement</span></span> | <span data-ttu-id="cd0c9-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd0c9-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0c9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd0c9-118">Header</span></span><br/> | <dl> <span data-ttu-id="cd0c9-119"><dt>Combase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd0c9-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd0c9-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd0c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd0c9-121">**CFactoryTemplate (clase)**</span><span class="sxs-lookup"><span data-stu-id="cd0c9-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




