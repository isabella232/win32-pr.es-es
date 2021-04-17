---
description: El método SetFormatType especifica el tipo de formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Método CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671223"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="34361-103">CMediaType. SetFormatType, método</span><span class="sxs-lookup"><span data-stu-id="34361-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="34361-104">El método ' ' SetFormatType especifica el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="34361-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="34361-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34361-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="34361-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34361-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="34361-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="34361-108">Puntero a un **GUID** que especifica el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="34361-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34361-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34361-109">Return value</span></span>

<span data-ttu-id="34361-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="34361-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34361-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34361-111">Remarks</span></span>

<span data-ttu-id="34361-112">Este método establece el miembro **formatType** .</span><span class="sxs-lookup"><span data-stu-id="34361-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="34361-113">El tipo de formato define el diseño del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="34361-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="34361-114">Por ejemplo, si el tipo de formato es FORMAT \_ info, el bloque de formato debe contener una estructura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="34361-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="34361-115">Para establecer el bloque de formato, llame al método [**CMediaType:: SetFormat**](cmediatype-setformat.md) .</span><span class="sxs-lookup"><span data-stu-id="34361-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="34361-116">El autor de la llamada es responsable de asegurarse de que el bloque de formato coincide con el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="34361-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="34361-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34361-117">Requirements</span></span>



| <span data-ttu-id="34361-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34361-118">Requirement</span></span> | <span data-ttu-id="34361-119">Value</span><span class="sxs-lookup"><span data-stu-id="34361-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34361-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34361-120">Header</span></span><br/>  | <dl> <span data-ttu-id="34361-121"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34361-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="34361-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34361-122">Library</span></span><br/> | <dl> <span data-ttu-id="34361-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="34361-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34361-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="34361-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34361-125">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="34361-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
