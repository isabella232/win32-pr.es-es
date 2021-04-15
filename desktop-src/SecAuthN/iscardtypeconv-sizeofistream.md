---
description: Determina el tamaño, en bytes, de la interfaz COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv:: SizeOfIStream (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648427"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="eecce-103">ISCardTypeConv:: SizeOfIStream (método)</span><span class="sxs-lookup"><span data-stu-id="eecce-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="eecce-104">\[El método **SizeOfIStream** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="eecce-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eecce-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eecce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eecce-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="eecce-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eecce-107">El método **SizeOfIStream** determina el tamaño, en bytes, de la interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="eecce-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecce-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eecce-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="eecce-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eecce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eecce-110">*pStrm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eecce-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eecce-111">Puntero a la interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="eecce-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="eecce-112">*puliSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eecce-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eecce-113">Puntero al entero grande sin signo que puede contener todo el valor de tamaño de bit 64 de la interfaz com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="eecce-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eecce-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eecce-114">Return value</span></span>

<span data-ttu-id="eecce-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="eecce-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="eecce-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eecce-116">Return code</span></span>                                                                                  | <span data-ttu-id="eecce-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="eecce-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eecce-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="eecce-119">La función se ejecutó correctamente y *\* puliSize* es el tamaño, en bytes, de la interfaz com IStream.</span><span class="sxs-lookup"><span data-stu-id="eecce-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="eecce-120"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="eecce-121">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="eecce-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="eecce-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="eecce-123">El parámetro *puliSize* es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="eecce-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="eecce-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="eecce-125">El parámetro *pStrm* es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="eecce-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="eecce-126"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="eecce-127">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="eecce-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="eecce-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eecce-128">Requirements</span></span>



| <span data-ttu-id="eecce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="eecce-129">Requirement</span></span> | <span data-ttu-id="eecce-130">Value</span><span class="sxs-lookup"><span data-stu-id="eecce-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eecce-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eecce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eecce-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="eecce-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eecce-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eecce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eecce-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="eecce-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eecce-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="eecce-135">End of client support</span></span><br/>    | <span data-ttu-id="eecce-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eecce-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eecce-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="eecce-137">End of server support</span></span><br/>    | <span data-ttu-id="eecce-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eecce-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eecce-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eecce-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="eecce-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="eecce-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eecce-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="eecce-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eecce-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eecce-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eecce-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eecce-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eecce-145">IID</span><span class="sxs-lookup"><span data-stu-id="eecce-145">IID</span></span><br/>                      | <span data-ttu-id="eecce-146">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="eecce-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eecce-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="eecce-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eecce-148">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="eecce-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="eecce-149">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="eecce-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
