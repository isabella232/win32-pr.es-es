---
description: El método Clone crea un nuevo objeto con su propio puntero de búsqueda que hace referencia a los mismos bytes que el objeto IByteBuffer original.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer:: Clone (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278140"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="f77a1-103">IByteBuffer:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="f77a1-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="f77a1-104">\[El método **Clone** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f77a1-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f77a1-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f77a1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f77a1-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f77a1-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f77a1-107">El método **Clone** crea un nuevo objeto con su propio puntero de búsqueda que hace referencia a los mismos bytes que el objeto [**IByteBuffer**](ibytebuffer.md) original.</span><span class="sxs-lookup"><span data-stu-id="f77a1-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f77a1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f77a1-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f77a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f77a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77a1-110">*ppByteBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f77a1-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f77a1-111">Cuando se realiza correctamente, apunta a la ubicación de un puntero [**IByteBuffer**](ibytebuffer.md) al nuevo objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f77a1-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="f77a1-112">Cuando haya terminado de usar el puntero **IByteBuffer** , suéltelo llamando a la función [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="f77a1-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="f77a1-113">Si se produce un error, este parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f77a1-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77a1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f77a1-114">Return value</span></span>

<span data-ttu-id="f77a1-115">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f77a1-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f77a1-116">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f77a1-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f77a1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f77a1-117">Remarks</span></span>

<span data-ttu-id="f77a1-118">Este método crea un nuevo objeto de secuencia para tener acceso a los mismos bytes, pero con un puntero de búsqueda independiente.</span><span class="sxs-lookup"><span data-stu-id="f77a1-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="f77a1-119">El nuevo objeto de flujo ve los mismos datos que el objeto de flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="f77a1-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="f77a1-120">Los cambios que se escriben en un objeto son visibles inmediatamente en el otro.</span><span class="sxs-lookup"><span data-stu-id="f77a1-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="f77a1-121">El bloqueo de intervalo se comparte entre los objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f77a1-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="f77a1-122">La configuración inicial del puntero de búsqueda en la instancia de la secuencia clonada es la misma que la configuración actual del puntero de búsqueda en la secuencia original en el momento de la operación de clonación.</span><span class="sxs-lookup"><span data-stu-id="f77a1-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="f77a1-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f77a1-123">Examples</span></span>

<span data-ttu-id="f77a1-124">En el ejemplo siguiente se muestra la clonación de la interfaz [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f77a1-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="f77a1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f77a1-125">Requirements</span></span>



| <span data-ttu-id="f77a1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f77a1-126">Requirement</span></span> | <span data-ttu-id="f77a1-127">Value</span><span class="sxs-lookup"><span data-stu-id="f77a1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f77a1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f77a1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f77a1-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f77a1-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f77a1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f77a1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f77a1-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f77a1-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f77a1-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f77a1-132">End of client support</span></span><br/>    | <span data-ttu-id="f77a1-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f77a1-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f77a1-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f77a1-134">End of server support</span></span><br/>    | <span data-ttu-id="f77a1-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f77a1-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f77a1-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f77a1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f77a1-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f77a1-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f77a1-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f77a1-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="f77a1-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f77a1-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f77a1-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f77a1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f77a1-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f77a1-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f77a1-142">IID</span><span class="sxs-lookup"><span data-stu-id="f77a1-142">IID</span></span><br/>                      | <span data-ttu-id="f77a1-143">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f77a1-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

