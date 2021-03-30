---
description: El método Write escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer:: Write (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912486"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="8c92c-103">IByteBuffer:: Write (método)</span><span class="sxs-lookup"><span data-stu-id="8c92c-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="8c92c-104">\[El método de **escritura** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8c92c-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c92c-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8c92c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8c92c-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="8c92c-107">El método **Write** escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="8c92c-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c92c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c92c-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="8c92c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c92c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c92c-110">*pByte* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c92c-111">Dirección del búfer que contiene los datos que se van a escribir en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="8c92c-112">Se debe proporcionar un puntero válido para este parámetro aunque *CB* sea cero.</span><span class="sxs-lookup"><span data-stu-id="8c92c-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c92c-113">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c92c-114">Número de bytes de datos que se intentan escribir en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="8c92c-115">Este parámetro puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="8c92c-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c92c-116">*pcbWritten* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c92c-117">Dirección de una variable **larga** donde este método escribe el número real de bytes escritos en el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="8c92c-118">El autor de la llamada puede establecer este puntero en **null**, en cuyo caso, este método no proporciona el número real de bytes escritos.</span><span class="sxs-lookup"><span data-stu-id="8c92c-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c92c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c92c-119">Return value</span></span>

<span data-ttu-id="8c92c-120">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8c92c-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="8c92c-121">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8c92c-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c92c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c92c-122">Remarks</span></span>

<span data-ttu-id="8c92c-123">El método **IByteBuffer:: Write** escribe los datos especificados en un objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="8c92c-124">El puntero de búsqueda se ajusta para el número de bytes escritos realmente.</span><span class="sxs-lookup"><span data-stu-id="8c92c-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="8c92c-125">El número de bytes escritos realmente se devuelve en el parámetro *pcbWritten* .</span><span class="sxs-lookup"><span data-stu-id="8c92c-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="8c92c-126">Si el recuento de bytes es cero bytes, la operación de escritura no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8c92c-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="8c92c-127">Si el puntero de búsqueda está actualmente más allá del final de la secuencia y el recuento de bytes es distinto de cero, este método aumenta el tamaño de la secuencia al puntero de búsqueda y escribe los bytes especificados a partir del puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8c92c-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="8c92c-128">Los bytes de relleno escritos en la secuencia no se inicializan en ningún valor determinado.</span><span class="sxs-lookup"><span data-stu-id="8c92c-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="8c92c-129">Esto es lo mismo que el comportamiento de final de archivo en el sistema de archivos FAT de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="8c92c-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="8c92c-130">Con un recuento de cero bytes y un puntero de búsqueda más allá del final de la secuencia, este método no crea los bytes de relleno para aumentar la secuencia al puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="8c92c-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="8c92c-131">En este caso, debe llamar al método [**IByteBuffer:: setSize**](ibytebuffer-setsize.md) para aumentar el tamaño de la secuencia y escribir los bytes de relleno.</span><span class="sxs-lookup"><span data-stu-id="8c92c-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="8c92c-132">El parámetro *pcbWritten* puede tener un valor incluso si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8c92c-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="8c92c-133">En la implementación proporcionada por COM, los objetos de secuencia no son dispersos.</span><span class="sxs-lookup"><span data-stu-id="8c92c-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="8c92c-134">Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="8c92c-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8c92c-135">Examples</span></span>

<span data-ttu-id="8c92c-136">En el ejemplo siguiente se muestra la escritura de bytes en el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c92c-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="8c92c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c92c-137">Requirements</span></span>



| <span data-ttu-id="8c92c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c92c-138">Requirement</span></span> | <span data-ttu-id="8c92c-139">Value</span><span class="sxs-lookup"><span data-stu-id="8c92c-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c92c-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c92c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8c92c-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c92c-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c92c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8c92c-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c92c-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c92c-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8c92c-144">End of client support</span></span><br/>    | <span data-ttu-id="8c92c-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c92c-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8c92c-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8c92c-146">End of server support</span></span><br/>    | <span data-ttu-id="8c92c-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c92c-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8c92c-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c92c-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c92c-149"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c92c-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c92c-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8c92c-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c92c-151"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c92c-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c92c-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c92c-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c92c-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c92c-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8c92c-154">IID</span><span class="sxs-lookup"><span data-stu-id="8c92c-154">IID</span></span><br/>                      | <span data-ttu-id="8c92c-155">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="8c92c-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

