---
description: Restringe el acceso a un intervalo de bytes especificado en el objeto de búfer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer:: LockRegion (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278582"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="a5998-103">IByteBuffer:: LockRegion (método)</span><span class="sxs-lookup"><span data-stu-id="a5998-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="a5998-104">\[El método **LockRegion** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a5998-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a5998-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5998-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a5998-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a5998-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a5998-107">El método **LockRegion** restringe el acceso a un intervalo de bytes especificado en el objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="a5998-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5998-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5998-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="a5998-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5998-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5998-110">*libOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5998-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5998-111">Entero que especifica el desplazamiento de bytes para el principio del intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5998-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="a5998-112">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5998-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5998-113">Entero que especifica la longitud del intervalo, en bytes, que se va a restringir.</span><span class="sxs-lookup"><span data-stu-id="a5998-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="a5998-114">*dwLockType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5998-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5998-115">Especifica las restricciones que se solicitan al tener acceso al intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5998-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="a5998-116">Puede ser uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5998-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="a5998-117">Value</span><span class="sxs-lookup"><span data-stu-id="a5998-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a5998-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a5998-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="a5998-119"><dt>**escritura de BLOQUEos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="a5998-120">El intervalo especificado de bytes se puede abrir y leer cualquier número de veces, pero la escritura en el intervalo bloqueado está prohibida, excepto para el propietario que concedió este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="a5998-121"><dt>**BLOQUEO \_ exclusivo**</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="a5998-122">La escritura en el intervalo de bytes especificado está prohibida, excepto para el propietario al que se concedió este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="a5998-123"><dt>**BLOQUEAR \_ ONLYONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="a5998-124">Si se concede este bloqueo, no \_ se puede obtener ningún otro bloqueo de ONLYONCE de bloqueo en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5998-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="a5998-125">Normalmente, este tipo de bloqueo es un alias para algún otro tipo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="a5998-126">Por lo tanto, las implementaciones específicas pueden tener un comportamiento adicional asociado a este tipo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5998-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5998-127">Return value</span></span>

<span data-ttu-id="a5998-128">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a5998-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a5998-129">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5998-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5998-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5998-130">Remarks</span></span>

<span data-ttu-id="a5998-131">El intervalo de bytes puede extenderse más allá del final actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a5998-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="a5998-132">El bloqueo más allá del final de una secuencia es útil como método de comunicación entre las distintas instancias de la secuencia sin cambiar los datos que realmente forman parte de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a5998-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="a5998-133">Se admiten tres tipos de bloqueo: el bloqueo para excluir otros escritores, el bloqueo para excluir otros lectores o escritores, y el bloqueo que permite a un solo solicitante obtener un bloqueo en el intervalo determinado, que suele ser un alias de uno de los otros dos tipos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="a5998-134">Una instancia de Stream determinada podría admitir cualquiera de los dos primeros tipos, o ambos.</span><span class="sxs-lookup"><span data-stu-id="a5998-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="a5998-135">El tipo de bloqueo se especifica mediante *dwLockType*, con un valor de la enumeración [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) .</span><span class="sxs-lookup"><span data-stu-id="a5998-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="a5998-136">Posteriormente, cualquier región bloqueada con **LockRegion** debe desbloquearse explícitamente llamando a [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) con exactamente los mismos valores para los parámetros *libOffset*, *CB* y *dwLockType* .</span><span class="sxs-lookup"><span data-stu-id="a5998-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="a5998-137">La región debe desbloquearse antes de que se libere la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a5998-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="a5998-138">Dos regiones adyacentes no se pueden bloquear por separado y, a continuación, desbloquearse con una sola llamada de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="a5998-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="a5998-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5998-139">Examples</span></span>

<span data-ttu-id="a5998-140">En el ejemplo siguiente se muestra cómo restringir el acceso a un intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="a5998-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="a5998-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5998-141">Requirements</span></span>



| <span data-ttu-id="a5998-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5998-142">Requirement</span></span> | <span data-ttu-id="a5998-143">Value</span><span class="sxs-lookup"><span data-stu-id="a5998-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5998-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5998-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a5998-145">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a5998-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a5998-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5998-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a5998-147">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5998-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5998-148">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a5998-148">End of client support</span></span><br/>    | <span data-ttu-id="a5998-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5998-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a5998-150">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a5998-150">End of server support</span></span><br/>    | <span data-ttu-id="a5998-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5998-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a5998-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5998-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5998-153"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5998-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a5998-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5998-155"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5998-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5998-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5998-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5998-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5998-158">IID</span><span class="sxs-lookup"><span data-stu-id="a5998-158">IID</span></span><br/>                      | <span data-ttu-id="a5998-159">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a5998-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

