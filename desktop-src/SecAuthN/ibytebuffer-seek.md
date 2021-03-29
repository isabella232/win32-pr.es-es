---
description: El método Seek cambia el puntero de búsqueda a una nueva ubicación con respecto al principio del búfer, al final del búfer o al puntero de búsqueda actual.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer:: Seek (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912489"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="2d10e-103">IByteBuffer:: Seek (método)</span><span class="sxs-lookup"><span data-stu-id="2d10e-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="2d10e-104">\[El método **Seek** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2d10e-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2d10e-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2d10e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d10e-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="2d10e-107">El método **Seek** cambia el puntero de búsqueda a una nueva ubicación con respecto al principio del búfer, al final del búfer o al puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="2d10e-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d10e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d10e-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="2d10e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d10e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d10e-110">*dlibMove* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d10e-111">Desplazamiento que se va a agregar a la ubicación indicada por *dwOrigin*.</span><span class="sxs-lookup"><span data-stu-id="2d10e-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="2d10e-112">Si *dwOrigin* es \_ el conjunto de búsqueda de secuencias \_ , se interpreta como un valor sin signo en lugar de con signo.</span><span class="sxs-lookup"><span data-stu-id="2d10e-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="2d10e-113">*dwOrigin* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d10e-114">Especifica el origen del desplazamiento especificado en *dlibMove*.</span><span class="sxs-lookup"><span data-stu-id="2d10e-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="2d10e-115">El origen puede ser uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2d10e-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="2d10e-116">Value</span><span class="sxs-lookup"><span data-stu-id="2d10e-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="2d10e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2d10e-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="2d10e-118"><dt>**\_conjunto de búsqueda de secuencias \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="2d10e-119">El nuevo puntero de búsqueda es un desplazamiento relativo al principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="2d10e-120">En este caso, el parámetro *dlibMove* es la nueva posición de búsqueda en relación con el principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="2d10e-121"><dt>**STREAM \_ Seek \_ CUR**</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="2d10e-122">El nuevo puntero de búsqueda es un desplazamiento relativo a la ubicación del puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="2d10e-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="2d10e-123">En este caso, el parámetro *dlibMove* es el desplazamiento con signo de la posición de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="2d10e-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="2d10e-124"><dt>**\_final de búsqueda de flujo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="2d10e-125">El nuevo puntero de búsqueda es un desplazamiento relativo al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="2d10e-126">En este caso, el parámetro *dlibMove* es la nueva posición de búsqueda en relación con el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="2d10e-127">*plibNewPosition* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d10e-128">Puntero a la ubicación donde este método escribe el valor del nuevo puntero de búsqueda desde el principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="2d10e-129">Puede establecer este puntero en **null** para indicar que no está interesado en este valor.</span><span class="sxs-lookup"><span data-stu-id="2d10e-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="2d10e-130">En este caso, este método no proporciona el nuevo puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2d10e-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d10e-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d10e-131">Return value</span></span>

<span data-ttu-id="2d10e-132">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2d10e-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="2d10e-133">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2d10e-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d10e-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d10e-134">Remarks</span></span>

<span data-ttu-id="2d10e-135">El método de **búsqueda** cambia el puntero de búsqueda, por lo que las operaciones de lectura y escritura posteriores pueden tener lugar en una ubicación diferente en el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="2d10e-136">Es un error buscar antes del principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="2d10e-137">No obstante, no se trata de un error para buscar más allá del final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d10e-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="2d10e-138">Buscar más allá del final de la secuencia es útil para las operaciones de escritura posteriores, ya que la secuencia en ese momento se extenderá a la posición de búsqueda inmediatamente antes de que se realice la operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="2d10e-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="2d10e-139">También puede usar este método para obtener el valor actual del puntero de búsqueda llamando a este método con el parámetro *dwOrigin* establecido en Stream \_ Seek \_ CUR y el parámetro *dlibMove* establecido en cero para que no se cambie el puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2d10e-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="2d10e-140">El puntero de búsqueda actual se devuelve en el parámetro *plibNewPosition* .</span><span class="sxs-lookup"><span data-stu-id="2d10e-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="2d10e-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2d10e-141">Examples</span></span>

<span data-ttu-id="2d10e-142">En el ejemplo siguiente se muestra cómo colocar el puntero de búsqueda a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="2d10e-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="2d10e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d10e-143">Requirements</span></span>



| <span data-ttu-id="2d10e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d10e-144">Requirement</span></span> | <span data-ttu-id="2d10e-145">Value</span><span class="sxs-lookup"><span data-stu-id="2d10e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d10e-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d10e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2d10e-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2d10e-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d10e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2d10e-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d10e-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d10e-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2d10e-150">End of client support</span></span><br/>    | <span data-ttu-id="2d10e-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d10e-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2d10e-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2d10e-152">End of server support</span></span><br/>    | <span data-ttu-id="2d10e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d10e-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2d10e-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d10e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d10e-155"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d10e-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2d10e-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d10e-157"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d10e-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d10e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d10e-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d10e-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d10e-160">IID</span><span class="sxs-lookup"><span data-stu-id="2d10e-160">IID</span></span><br/>                      | <span data-ttu-id="2d10e-161">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="2d10e-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

