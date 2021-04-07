---
description: 'Quita la restricción de acceso de un intervalo de bytes previamente restringido mediante IByteBuffer:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'IByteBuffer:: UnlockRegion (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002757"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="f917f-103">IByteBuffer:: UnlockRegion (método)</span><span class="sxs-lookup"><span data-stu-id="f917f-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="f917f-104">\[El método **UnlockRegion** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f917f-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f917f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f917f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f917f-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f917f-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f917f-107">El método **UnlockRegion** quita la restricción de acceso de un intervalo de bytes previamente restringido mediante [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="f917f-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f917f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f917f-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="f917f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f917f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f917f-110">*libOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917f-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f917f-111">Desplazamiento de bytes para el principio del intervalo.</span><span class="sxs-lookup"><span data-stu-id="f917f-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="f917f-112">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917f-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f917f-113">Longitud, en bytes, del intervalo que se va a restringir.</span><span class="sxs-lookup"><span data-stu-id="f917f-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="f917f-114">*dwLockType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f917f-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f917f-115">Restricciones de acceso previamente colocadas en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="f917f-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f917f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f917f-116">Return value</span></span>

<span data-ttu-id="f917f-117">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f917f-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f917f-118">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f917f-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f917f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f917f-119">Remarks</span></span>

<span data-ttu-id="f917f-120">El método **IByteBuffer:: UnlockRegion** desbloquea una región bloqueada previamente con el método [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md) .</span><span class="sxs-lookup"><span data-stu-id="f917f-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="f917f-121">Las regiones bloqueadas se deben desbloquear más adelante de forma explícita llamando a **IByteBuffer:: UnlockRegion** con exactamente los mismos valores para los parámetros *libOffset*, *CB* y *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="f917f-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="f917f-122">La región debe desbloquearse antes de que se libere la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f917f-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="f917f-123">Dos regiones adyacentes no se pueden bloquear por separado y, a continuación, desbloquearse con una sola llamada de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="f917f-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="f917f-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f917f-124">Examples</span></span>

<span data-ttu-id="f917f-125">En el ejemplo siguiente se muestra cómo desbloquear un intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f917f-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="f917f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f917f-126">Requirements</span></span>



| <span data-ttu-id="f917f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f917f-127">Requirement</span></span> | <span data-ttu-id="f917f-128">Value</span><span class="sxs-lookup"><span data-stu-id="f917f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f917f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f917f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f917f-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f917f-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f917f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f917f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f917f-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f917f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f917f-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f917f-133">End of client support</span></span><br/>    | <span data-ttu-id="f917f-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f917f-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f917f-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f917f-135">End of server support</span></span><br/>    | <span data-ttu-id="f917f-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f917f-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f917f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f917f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f917f-138"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f917f-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f917f-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f917f-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f917f-140"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f917f-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f917f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f917f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f917f-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f917f-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f917f-143">IID</span><span class="sxs-lookup"><span data-stu-id="f917f-143">IID</span></span><br/>                      | <span data-ttu-id="f917f-144">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f917f-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

