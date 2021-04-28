---
description: 'CUnknown::m_cRef miembro: recuento de referencias.'
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: CUnknown::m_cRef miembro (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084583"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="9baca-103">Miembro CUnknown::m \_ cRef</span><span class="sxs-lookup"><span data-stu-id="9baca-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="9baca-104">Recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="9baca-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="9baca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9baca-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="9baca-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9baca-106">Remarks</span></span>

<span data-ttu-id="9baca-107">Use esta variable miembro si invalida el [**método NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) [**o NonDelegatingRelease.**](cunknown-nondelegatingrelease.md)</span><span class="sxs-lookup"><span data-stu-id="9baca-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9baca-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9baca-108">Requirements</span></span>



| <span data-ttu-id="9baca-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="9baca-109">Requirement</span></span> | <span data-ttu-id="9baca-110">Value</span><span class="sxs-lookup"><span data-stu-id="9baca-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9baca-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9baca-111">Header</span></span><br/>  | <dl> <span data-ttu-id="9baca-112"><dt>Combase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9baca-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9baca-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9baca-113">Library</span></span><br/> | <dl> <span data-ttu-id="9baca-114"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9baca-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




