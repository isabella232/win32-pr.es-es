---
description: Crea una matriz SAFEARRAY de automatización de caracteres sin signo (bytes).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'ISCardTypeConv:: CreateSafeArray (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153735"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="ff565-103">ISCardTypeConv:: CreateSafeArray (método)</span><span class="sxs-lookup"><span data-stu-id="ff565-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="ff565-104">\[El método **CreateSafeArray** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ff565-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ff565-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff565-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ff565-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ff565-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ff565-107">El método **CreateSafeArray** crea una matriz SafeArray de automatización de caracteres sin signo (bytes).</span><span class="sxs-lookup"><span data-stu-id="ff565-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff565-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff565-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="ff565-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff565-110">*nAllocSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff565-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff565-111">Tamaño en bytes de la memoria que se va a asignar para la matriz.</span><span class="sxs-lookup"><span data-stu-id="ff565-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="ff565-112">*ppArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ff565-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff565-113">Puntero al objeto SAFEARRAY que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="ff565-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff565-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff565-114">Return value</span></span>

<span data-ttu-id="ff565-115">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="ff565-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="ff565-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ff565-116">Return code</span></span>                                                                                   | <span data-ttu-id="ff565-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff565-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff565-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ff565-119">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff565-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ff565-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ff565-121">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="ff565-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="ff565-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ff565-123">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff565-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ff565-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff565-124">Remarks</span></span>

<span data-ttu-id="ff565-125">Para crear una matriz de bytes de C/C++ típica, llame a [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="ff565-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="ff565-126">Para crear un búfer universal de bytes asignado en un objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)), llame a [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ff565-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff565-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff565-127">Requirements</span></span>



| <span data-ttu-id="ff565-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff565-128">Requirement</span></span> | <span data-ttu-id="ff565-129">Value</span><span class="sxs-lookup"><span data-stu-id="ff565-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff565-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff565-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff565-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ff565-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ff565-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff565-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff565-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff565-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff565-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ff565-134">End of client support</span></span><br/>    | <span data-ttu-id="ff565-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff565-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ff565-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ff565-136">End of server support</span></span><br/>    | <span data-ttu-id="ff565-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff565-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ff565-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff565-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff565-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff565-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ff565-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff565-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff565-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff565-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff565-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff565-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff565-144">IID</span><span class="sxs-lookup"><span data-stu-id="ff565-144">IID</span></span><br/>                      | <span data-ttu-id="ff565-145">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ff565-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ff565-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff565-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff565-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="ff565-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="ff565-148">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="ff565-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="ff565-149">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="ff565-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="ff565-150">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="ff565-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
