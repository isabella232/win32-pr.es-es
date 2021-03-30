---
description: El método setSize cambia el tamaño del objeto de secuencia.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer:: setSize (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002758"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="73330-103">IByteBuffer:: setSize (método)</span><span class="sxs-lookup"><span data-stu-id="73330-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="73330-104">\[El método **setSize** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="73330-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="73330-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73330-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="73330-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="73330-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="73330-107">El método **setSize** cambia el tamaño del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="73330-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="73330-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73330-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="73330-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73330-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73330-110">*libNewSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73330-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73330-111">Nuevo tamaño de la secuencia como un número de bytes</span><span class="sxs-lookup"><span data-stu-id="73330-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73330-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73330-112">Return value</span></span>

<span data-ttu-id="73330-113">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="73330-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="73330-114">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="73330-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="73330-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73330-115">Remarks</span></span>

<span data-ttu-id="73330-116">El método **IByteBuffer:: setSize** cambia el tamaño del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="73330-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="73330-117">Llame a este método para asignar previamente espacio para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73330-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="73330-118">Si el parámetro *libNewSize* es mayor que el tamaño de la secuencia actual, el flujo se extiende hasta el tamaño indicado rellenando el espacio intermedio con bytes de valor sin definir.</span><span class="sxs-lookup"><span data-stu-id="73330-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="73330-119">Esta operación es similar al método [**IByteBuffer:: Write**](ibytebuffer-write.md) si el puntero de búsqueda está más allá del final actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73330-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="73330-120">Si el parámetro *libNewSize* es menor que el flujo actual, el flujo se trunca al tamaño indicado.</span><span class="sxs-lookup"><span data-stu-id="73330-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="73330-121">El puntero de búsqueda no se ve afectado por el cambio en el tamaño de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73330-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="73330-122">Llamar a **IByteBuffer:: setSize** puede ser una manera eficaz de intentar obtener un gran fragmento de espacio contiguo.</span><span class="sxs-lookup"><span data-stu-id="73330-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="73330-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="73330-123">Examples</span></span>

<span data-ttu-id="73330-124">En el ejemplo siguiente se muestra cómo establecer el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="73330-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="73330-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73330-125">Requirements</span></span>



| <span data-ttu-id="73330-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="73330-126">Requirement</span></span> | <span data-ttu-id="73330-127">Value</span><span class="sxs-lookup"><span data-stu-id="73330-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73330-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73330-128">Minimum supported client</span></span><br/> | <span data-ttu-id="73330-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="73330-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="73330-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73330-130">Minimum supported server</span></span><br/> | <span data-ttu-id="73330-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73330-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73330-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="73330-132">End of client support</span></span><br/>    | <span data-ttu-id="73330-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="73330-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="73330-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="73330-134">End of server support</span></span><br/>    | <span data-ttu-id="73330-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73330-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="73330-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73330-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="73330-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="73330-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="73330-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="73330-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="73330-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73330-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73330-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73330-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73330-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73330-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="73330-142">IID</span><span class="sxs-lookup"><span data-stu-id="73330-142">IID</span></span><br/>                      | <span data-ttu-id="73330-143">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="73330-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

