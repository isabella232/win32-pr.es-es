---
description: El método siguiente obtiene el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant:: Next (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691010"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="f35cf-104">IEnumParticipant:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="f35cf-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="f35cf-105">\[**Next** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f35cf-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f35cf-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f35cf-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f35cf-107">El método **siguiente** obtiene el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f35cf-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="f35cf-108">Este método está oculto en Visual Basic y en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="f35cf-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35cf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f35cf-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="f35cf-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f35cf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f35cf-111">*Celt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f35cf-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f35cf-112">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="f35cf-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="f35cf-113">*ppElements* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f35cf-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f35cf-114">Puntero a las interfaces de [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .</span><span class="sxs-lookup"><span data-stu-id="f35cf-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="f35cf-115">*pceltFetched* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f35cf-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f35cf-116">Puntero al número de elementos proporcionados realmente.</span><span class="sxs-lookup"><span data-stu-id="f35cf-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="f35cf-117">Puede ser **null** si *Celt* es uno.</span><span class="sxs-lookup"><span data-stu-id="f35cf-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f35cf-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f35cf-118">Return value</span></span>

<span data-ttu-id="f35cf-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f35cf-119">This method can return one of these values.</span></span>



| <span data-ttu-id="f35cf-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f35cf-120">Return code</span></span>                                                                                   | <span data-ttu-id="f35cf-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f35cf-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f35cf-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f35cf-123">El método devolvió un número de elementos de *Celt* .</span><span class="sxs-lookup"><span data-stu-id="f35cf-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="f35cf-124"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="f35cf-125">El número de elementos restantes era menor que *Celt*.</span><span class="sxs-lookup"><span data-stu-id="f35cf-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="f35cf-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f35cf-127">El parámetro *ppElements* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="f35cf-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f35cf-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f35cf-129">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f35cf-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f35cf-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f35cf-130">Remarks</span></span>

<span data-ttu-id="f35cf-131">TAPI llama al método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la interfaz [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) devuelta por **IEnumParticipant:: Next**.</span><span class="sxs-lookup"><span data-stu-id="f35cf-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="f35cf-132">La aplicación debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la interfaz **ITAgentHandler** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="f35cf-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f35cf-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f35cf-133">Requirements</span></span>



| <span data-ttu-id="f35cf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f35cf-134">Requirement</span></span> | <span data-ttu-id="f35cf-135">Value</span><span class="sxs-lookup"><span data-stu-id="f35cf-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f35cf-136">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f35cf-136">TAPI version</span></span><br/> | <span data-ttu-id="f35cf-137">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f35cf-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f35cf-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f35cf-138">Header</span></span><br/>       | <dl> <span data-ttu-id="f35cf-139"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="f35cf-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f35cf-140">Library</span></span><br/>      | <dl> <span data-ttu-id="f35cf-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f35cf-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f35cf-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="f35cf-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f35cf-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f35cf-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f35cf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35cf-145">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="f35cf-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="f35cf-146">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="f35cf-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

