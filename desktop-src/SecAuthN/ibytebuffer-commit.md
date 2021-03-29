---
description: El método commit garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento principal.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer:: Commit (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648567"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="bf57d-103">IByteBuffer:: Commit (método)</span><span class="sxs-lookup"><span data-stu-id="bf57d-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="bf57d-104">\[El método **commit** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bf57d-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf57d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bf57d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bf57d-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="bf57d-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="bf57d-107">El método **commit** garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento principal.</span><span class="sxs-lookup"><span data-stu-id="bf57d-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf57d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf57d-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bf57d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf57d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf57d-110">*grfCommitFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bf57d-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf57d-111">Controla la forma en que se confirman los cambios realizados en un objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="bf57d-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="bf57d-112">Para obtener una definición de estos valores, consulte la enumeración STGC.</span><span class="sxs-lookup"><span data-stu-id="bf57d-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf57d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf57d-113">Return value</span></span>

<span data-ttu-id="bf57d-114">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bf57d-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="bf57d-115">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bf57d-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf57d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf57d-116">Remarks</span></span>

<span data-ttu-id="bf57d-117">Este método garantiza que los cambios en un objeto de secuencia abierto en modo de transacción se reflejan en el almacenamiento primario.</span><span class="sxs-lookup"><span data-stu-id="bf57d-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="bf57d-118">Los cambios que se han realizado en la secuencia desde que se abrió o se confirmó por última vez se reflejan en el objeto de almacenamiento primario.</span><span class="sxs-lookup"><span data-stu-id="bf57d-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="bf57d-119">Si el elemento primario está abierto en modo de transacción, el elemento primario todavía puede revertir en un momento posterior revirtiendo los cambios en este objeto de flujo.</span><span class="sxs-lookup"><span data-stu-id="bf57d-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="bf57d-120">La implementación de archivo compuesto no admite la apertura de secuencias en modo de transacción, por lo que este método tiene muy poco efecto que el vaciado de búferes de memoria.</span><span class="sxs-lookup"><span data-stu-id="bf57d-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="bf57d-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf57d-121">Examples</span></span>

<span data-ttu-id="bf57d-122">En el ejemplo siguiente se muestra la confirmación de cambios en el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="bf57d-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="bf57d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf57d-123">Requirements</span></span>



| <span data-ttu-id="bf57d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf57d-124">Requirement</span></span> | <span data-ttu-id="bf57d-125">Value</span><span class="sxs-lookup"><span data-stu-id="bf57d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf57d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf57d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bf57d-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bf57d-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bf57d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf57d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bf57d-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf57d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf57d-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bf57d-130">End of client support</span></span><br/>    | <span data-ttu-id="bf57d-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf57d-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bf57d-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bf57d-132">End of server support</span></span><br/>    | <span data-ttu-id="bf57d-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf57d-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bf57d-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf57d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf57d-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf57d-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf57d-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bf57d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf57d-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf57d-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf57d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf57d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf57d-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf57d-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf57d-140">IID</span><span class="sxs-lookup"><span data-stu-id="bf57d-140">IID</span></span><br/>                      | <span data-ttu-id="bf57d-141">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="bf57d-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

