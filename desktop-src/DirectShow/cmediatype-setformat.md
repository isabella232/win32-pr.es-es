---
description: El método SetFormat inicializa el bloque de formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Método CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680483"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="729f6-103">CMediaType. SetFormat, método</span><span class="sxs-lookup"><span data-stu-id="729f6-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="729f6-104">El `SetFormat` método inicializa el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="729f6-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="729f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="729f6-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="729f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="729f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729f6-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="729f6-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="729f6-108">Puntero a un bloque de memoria que contiene el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="729f6-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="729f6-109">*length*</span><span class="sxs-lookup"><span data-stu-id="729f6-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="729f6-110">Longitud del bloque de formato, en bytes.</span><span class="sxs-lookup"><span data-stu-id="729f6-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="729f6-111">Return value</span></span>

<span data-ttu-id="729f6-112">Devuelve **true si es** correcto, o **false** si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="729f6-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="729f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="729f6-113">Remarks</span></span>

<span data-ttu-id="729f6-114">Este método asigna memoria para el bloque de formato y copia el búfer especificado por *pFormat* en el nuevo bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="729f6-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="729f6-115">Si el tipo de medio ya contiene un bloque de formato, se libera el anterior.</span><span class="sxs-lookup"><span data-stu-id="729f6-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="729f6-116">El método también establece el miembro **cbFormat** de la estructura de **\_ \_ tipo de medio am** .</span><span class="sxs-lookup"><span data-stu-id="729f6-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="729f6-117">Para establecer el tipo de formato, llame al método [**CMediaType:: SetFormatType**](cmediatype-setformattype.md) .</span><span class="sxs-lookup"><span data-stu-id="729f6-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="729f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="729f6-118">Requirements</span></span>



| <span data-ttu-id="729f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="729f6-119">Requirement</span></span> | <span data-ttu-id="729f6-120">Value</span><span class="sxs-lookup"><span data-stu-id="729f6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="729f6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="729f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="729f6-122"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="729f6-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="729f6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="729f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="729f6-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="729f6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="729f6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="729f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729f6-126">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="729f6-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




