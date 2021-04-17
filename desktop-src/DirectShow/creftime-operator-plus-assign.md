---
description: El operador + = agrega dos tiempos de referencia.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: Método CRefTime. Operator + = (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660726"
---
# <a name="creftimeoperator-method"></a><span data-ttu-id="61785-103">CRefTime. Operator + = (método)</span><span class="sxs-lookup"><span data-stu-id="61785-103">CRefTime.operator+= method</span></span>

<span data-ttu-id="61785-104">El operador + = agrega dos tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="61785-104">The += operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="61785-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61785-105">Syntax</span></span>


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="61785-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61785-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="61785-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="61785-108">Referencia a un objeto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="61785-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61785-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61785-109">Return value</span></span>

<span data-ttu-id="61785-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="61785-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="61785-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61785-111">Requirements</span></span>



| <span data-ttu-id="61785-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="61785-112">Requirement</span></span> | <span data-ttu-id="61785-113">Value</span><span class="sxs-lookup"><span data-stu-id="61785-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61785-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61785-114">Header</span></span><br/>  | <dl> <span data-ttu-id="61785-115"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61785-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61785-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61785-116">Library</span></span><br/> | <dl> <span data-ttu-id="61785-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="61785-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




