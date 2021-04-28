---
description: 'Constructor CMediaControl.CMediaControl: método constructor.'
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Constructor CMediaControl.CMediaControl (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099213"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="3da26-103">Constructor CMediaControl.CMediaControl</span><span class="sxs-lookup"><span data-stu-id="3da26-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="3da26-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="3da26-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3da26-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3da26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3da26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da26-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3da26-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3da26-108">Puntero al nombre del objeto con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="3da26-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="3da26-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="3da26-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3da26-110">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="3da26-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3da26-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3da26-111">Remarks</span></span>

<span data-ttu-id="3da26-112">Asigne el *parámetro pName* en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="3da26-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="3da26-113">Este nombre aparece en el terminal de depuración tras la creación y eliminación del objeto.</span><span class="sxs-lookup"><span data-stu-id="3da26-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da26-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da26-114">Requirements</span></span>



| <span data-ttu-id="3da26-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da26-115">Requirement</span></span> | <span data-ttu-id="3da26-116">Value</span><span class="sxs-lookup"><span data-stu-id="3da26-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da26-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3da26-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3da26-118"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3da26-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3da26-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3da26-119">Library</span></span><br/> | <dl> <span data-ttu-id="3da26-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3da26-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da26-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3da26-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da26-122">**CMediaControl (clase)**</span><span class="sxs-lookup"><span data-stu-id="3da26-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




