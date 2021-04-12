---
description: El método Read Lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer:: Read (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278580"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="22b59-103">IByteBuffer:: Read (método)</span><span class="sxs-lookup"><span data-stu-id="22b59-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="22b59-104">\[El método **Read** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="22b59-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22b59-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="22b59-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22b59-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="22b59-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="22b59-107">El método **Read** Lee un número especificado de bytes del objeto de búfer en la memoria a partir del puntero de búsqueda actual.</span><span class="sxs-lookup"><span data-stu-id="22b59-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b59-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22b59-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="22b59-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22b59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b59-110">*pByte* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22b59-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b59-111">Apunta al búfer en el que se leen los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="22b59-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="22b59-112">Si se produce un error, este valor es **null**.</span><span class="sxs-lookup"><span data-stu-id="22b59-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="22b59-113">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22b59-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b59-114">Número de bytes de datos que se intentan leer del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="22b59-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="22b59-115">*pcbRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="22b59-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b59-116">Dirección de una variable **larga** que recibe el número real de bytes leídos del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="22b59-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="22b59-117">Puede establecer este puntero en **null** para indicar que no está interesado en este valor.</span><span class="sxs-lookup"><span data-stu-id="22b59-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="22b59-118">En este caso, este método no proporciona el número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="22b59-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b59-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22b59-119">Return value</span></span>

<span data-ttu-id="22b59-120">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22b59-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="22b59-121">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="22b59-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b59-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22b59-122">Remarks</span></span>

<span data-ttu-id="22b59-123">Este método lee los bytes de este objeto de secuencia en la memoria.</span><span class="sxs-lookup"><span data-stu-id="22b59-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="22b59-124">El objeto de secuencia debe estar abierto en el \_ modo de lectura STGM.</span><span class="sxs-lookup"><span data-stu-id="22b59-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="22b59-125">Este método ajusta el puntero de búsqueda por el número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="22b59-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="22b59-126">El número de bytes realmente leídos también se devuelve en el parámetro *pcbRead* .</span><span class="sxs-lookup"><span data-stu-id="22b59-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="22b59-127">Notas a los autores de las llamadas</span><span class="sxs-lookup"><span data-stu-id="22b59-127">Notes to Callers</span></span>

<span data-ttu-id="22b59-128">El número real de bytes leídos puede ser menor que el número de bytes solicitado si se produce un error o si se alcanza el final de la secuencia durante la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="22b59-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="22b59-129">Es posible que algunas implementaciones devuelvan un error si se alcanza el final de la secuencia durante la lectura.</span><span class="sxs-lookup"><span data-stu-id="22b59-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="22b59-130">Debe estar preparado para tratar con los valores devueltos de error devueltos o \_ de aceptar al final de las lecturas de flujo.</span><span class="sxs-lookup"><span data-stu-id="22b59-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="22b59-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="22b59-131">Examples</span></span>

<span data-ttu-id="22b59-132">En el ejemplo siguiente se muestra cómo leer bytes del búfer.</span><span class="sxs-lookup"><span data-stu-id="22b59-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="22b59-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22b59-133">Requirements</span></span>



| <span data-ttu-id="22b59-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b59-134">Requirement</span></span> | <span data-ttu-id="22b59-135">Value</span><span class="sxs-lookup"><span data-stu-id="22b59-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22b59-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22b59-136">Minimum supported client</span></span><br/> | <span data-ttu-id="22b59-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="22b59-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="22b59-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22b59-138">Minimum supported server</span></span><br/> | <span data-ttu-id="22b59-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22b59-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22b59-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="22b59-140">End of client support</span></span><br/>    | <span data-ttu-id="22b59-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="22b59-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="22b59-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="22b59-142">End of server support</span></span><br/>    | <span data-ttu-id="22b59-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22b59-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="22b59-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22b59-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="22b59-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b59-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22b59-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="22b59-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="22b59-147"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22b59-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22b59-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22b59-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22b59-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22b59-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="22b59-150">IID</span><span class="sxs-lookup"><span data-stu-id="22b59-150">IID</span></span><br/>                      | <span data-ttu-id="22b59-151">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="22b59-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

