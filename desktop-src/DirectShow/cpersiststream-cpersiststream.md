---
description: 'Constructor CPersistStream.CPersistStream: método constructor.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Constructor CPersistStream.CPersistStream (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085613"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="b64fa-103">Constructor CPersistStream.CPersistStream</span><span class="sxs-lookup"><span data-stu-id="b64fa-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="b64fa-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="b64fa-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b64fa-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b64fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b64fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64fa-107">*Punk*</span><span class="sxs-lookup"><span data-stu-id="b64fa-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b64fa-108">Puntero a **la interfaz IUnknown** del objeto de delegación.</span><span class="sxs-lookup"><span data-stu-id="b64fa-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="b64fa-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b64fa-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b64fa-110">Puntero al valor devuelto com general.</span><span class="sxs-lookup"><span data-stu-id="b64fa-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="b64fa-111">Este valor solo se cambia si se produce un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="b64fa-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b64fa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64fa-112">Requirements</span></span>



| <span data-ttu-id="b64fa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64fa-113">Requirement</span></span> | <span data-ttu-id="b64fa-114">Value</span><span class="sxs-lookup"><span data-stu-id="b64fa-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64fa-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b64fa-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b64fa-116"><dt>Pstream.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b64fa-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b64fa-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b64fa-117">Library</span></span><br/> | <dl> <span data-ttu-id="b64fa-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b64fa-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64fa-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b64fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64fa-120">**CPersistStream (clase)**</span><span class="sxs-lookup"><span data-stu-id="b64fa-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




