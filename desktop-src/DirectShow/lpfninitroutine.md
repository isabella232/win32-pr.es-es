---
description: Puntero a una función a la que se llama desde el punto de entrada de DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntero a la función LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679470"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="d0007-103">Puntero a la función LPFNInitRoutine</span><span class="sxs-lookup"><span data-stu-id="d0007-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="d0007-104">Puntero a una función a la que se llama desde el punto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="d0007-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0007-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0007-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="d0007-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0007-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0007-107">*bLoading*</span><span class="sxs-lookup"><span data-stu-id="d0007-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="d0007-108">**True** cuando se carga el archivo dll, **false** cuando se descarga el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="d0007-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="d0007-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="d0007-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="d0007-110">Puntero a la CLISD del objeto, que se especifica en la variable miembro [**CFactoryTemplate:: m \_ ClsID**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="d0007-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0007-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0007-111">Return value</span></span>

<span data-ttu-id="d0007-112">Este puntero de función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d0007-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0007-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0007-113">Requirements</span></span>



| <span data-ttu-id="d0007-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0007-114">Requirement</span></span> | <span data-ttu-id="d0007-115">Value</span><span class="sxs-lookup"><span data-stu-id="d0007-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0007-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0007-116">Header</span></span><br/> | <dl> <span data-ttu-id="d0007-117"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0007-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0007-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0007-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0007-119">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="d0007-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




