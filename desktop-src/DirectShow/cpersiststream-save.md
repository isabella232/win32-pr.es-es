---
description: Guarda los datos del filtro en la secuencia especificada.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Método CPersistStream. Save (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670996"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="2b95e-103">CPersistStream. Save (método)</span><span class="sxs-lookup"><span data-stu-id="2b95e-103">CPersistStream.Save method</span></span>

<span data-ttu-id="2b95e-104">Guarda los datos del filtro en la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="2b95e-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b95e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b95e-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="2b95e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b95e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b95e-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="2b95e-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="2b95e-108">Puntero a la secuencia en la que se van a guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="2b95e-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="2b95e-109">*fClearDirty*</span><span class="sxs-lookup"><span data-stu-id="2b95e-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="2b95e-110">Marca que indica si se debe restablecer la marca de modificado del flujo actual; **True** significa que se va a restablecer.</span><span class="sxs-lookup"><span data-stu-id="2b95e-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="2b95e-111">(Cuando se llama al método como parte de una operación de guardar, el valor suele ser **true**; cuando se llama como parte de una operación Guardar como, el valor suele ser **false**).</span><span class="sxs-lookup"><span data-stu-id="2b95e-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b95e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b95e-112">Return value</span></span>

<span data-ttu-id="2b95e-113">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b95e-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b95e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b95e-114">Remarks</span></span>

<span data-ttu-id="2b95e-115">Esta función miembro implementa el método **IPersistStream:: Save** .</span><span class="sxs-lookup"><span data-stu-id="2b95e-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="2b95e-116">Llama a **WriteInt** con la versión de software, llama a [**CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) con la secuencia en *pStm* y restablece **mPS \_ fDirty**.</span><span class="sxs-lookup"><span data-stu-id="2b95e-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b95e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b95e-117">Requirements</span></span>



| <span data-ttu-id="2b95e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b95e-118">Requirement</span></span> | <span data-ttu-id="2b95e-119">Value</span><span class="sxs-lookup"><span data-stu-id="2b95e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b95e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b95e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2b95e-121"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b95e-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b95e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b95e-122">Library</span></span><br/> | <dl> <span data-ttu-id="2b95e-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2b95e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b95e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b95e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b95e-125">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="2b95e-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




