---
description: Crea una matriz de bytes de C/C++ típica.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'ISCardTypeConv:: CreateByteArray (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156573"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="3190b-103">ISCardTypeConv:: CreateByteArray (método)</span><span class="sxs-lookup"><span data-stu-id="3190b-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="3190b-104">\[El método **CreateByteArray** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3190b-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3190b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3190b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3190b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3190b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3190b-107">El método **CreateByteArray** crea una matriz de bytes de C/C++ típica.</span><span class="sxs-lookup"><span data-stu-id="3190b-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="3190b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3190b-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="3190b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3190b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3190b-110">*dwAllocSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3190b-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3190b-111">Tamaño (en bytes) de la memoria que se va a asignar para la matriz.</span><span class="sxs-lookup"><span data-stu-id="3190b-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="3190b-112">*ppbyArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3190b-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3190b-113">Puntero a la matriz de bytes que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="3190b-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3190b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3190b-114">Return value</span></span>

<span data-ttu-id="3190b-115">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="3190b-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="3190b-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3190b-116">Return code</span></span>                                                                                   | <span data-ttu-id="3190b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3190b-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3190b-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3190b-119">Memoria asignada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3190b-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3190b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3190b-121">Hay un problema con uno o varios de los parámetros pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="3190b-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="3190b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3190b-123">No hay suficiente memoria libre para satisfacer la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3190b-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3190b-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3190b-124">Remarks</span></span>

<span data-ttu-id="3190b-125">Para crear un búfer universal de bytes asignado en un objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)), llame a [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3190b-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="3190b-126">Para crear una matriz SAFEARRAY de Automation de caracteres sin signo (bytes), llame a [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="3190b-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3190b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3190b-127">Requirements</span></span>



| <span data-ttu-id="3190b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3190b-128">Requirement</span></span> | <span data-ttu-id="3190b-129">Value</span><span class="sxs-lookup"><span data-stu-id="3190b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3190b-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3190b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3190b-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3190b-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3190b-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3190b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3190b-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3190b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3190b-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3190b-134">End of client support</span></span><br/>    | <span data-ttu-id="3190b-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3190b-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3190b-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3190b-136">End of server support</span></span><br/>    | <span data-ttu-id="3190b-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3190b-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3190b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3190b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3190b-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="3190b-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3190b-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="3190b-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3190b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3190b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3190b-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3190b-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3190b-144">IID</span><span class="sxs-lookup"><span data-stu-id="3190b-144">IID</span></span><br/>                      | <span data-ttu-id="3190b-145">IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3190b-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3190b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3190b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3190b-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="3190b-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="3190b-148">Valores devueltos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="3190b-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="3190b-149">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="3190b-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="3190b-150">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="3190b-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
