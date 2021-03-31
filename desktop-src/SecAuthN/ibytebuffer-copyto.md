---
description: El método CopyTo copia un número especificado de bytes del puntero de búsqueda actual del objeto en el puntero de búsqueda actual de otro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Método IByteBuffer:: CopyTo (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278585"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="9b1e1-103">IByteBuffer:: CopyTo (método)</span><span class="sxs-lookup"><span data-stu-id="9b1e1-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="9b1e1-104">\[El método **CopyTo** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9b1e1-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9b1e1-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="9b1e1-107">El método **CopyTo** copia un número especificado de bytes del puntero de búsqueda actual del objeto en el puntero de búsqueda actual de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b1e1-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="9b1e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b1e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b1e1-110">*pByteBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1e1-111">Apunta a la secuencia de destino.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-111">Points to the destination stream.</span></span> <span data-ttu-id="9b1e1-112">La secuencia a la que apunta *pByteBuffer* puede ser una nueva secuencia o un clon de la secuencia de origen.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="9b1e1-113">*CB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1e1-114">Número de bytes que se van a copiar desde el flujo de origen.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="9b1e1-115">*pcbRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1e1-116">Puntero a la ubicación donde este método escribe el número real de bytes leídos del origen.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="9b1e1-117">Puede establecer este puntero en **null** para indicar que no está interesado en este valor.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="9b1e1-118">En este caso, este método no proporciona el número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="9b1e1-119">*pcbWritten* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b1e1-120">Puntero a la ubicación donde este método escribe el número real de bytes escritos en el destino.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="9b1e1-121">Puede establecer este puntero en **null** para indicar que no está interesado en este valor.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="9b1e1-122">En este caso, este método no proporciona el número real de bytes escritos.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b1e1-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b1e1-123">Return value</span></span>

<span data-ttu-id="9b1e1-124">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="9b1e1-125">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b1e1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b1e1-126">Remarks</span></span>

<span data-ttu-id="9b1e1-127">Este método copia los bytes especificados de una secuencia a otra.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="9b1e1-128">También se puede usar para copiar un flujo en sí mismo.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="9b1e1-129">El puntero de búsqueda en cada instancia de Stream se ajusta para el número de bytes leídos o escritos.</span><span class="sxs-lookup"><span data-stu-id="9b1e1-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b1e1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b1e1-130">Requirements</span></span>



| <span data-ttu-id="9b1e1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b1e1-131">Requirement</span></span> | <span data-ttu-id="9b1e1-132">Value</span><span class="sxs-lookup"><span data-stu-id="9b1e1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b1e1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b1e1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9b1e1-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b1e1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b1e1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9b1e1-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b1e1-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b1e1-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9b1e1-137">End of client support</span></span><br/>    | <span data-ttu-id="9b1e1-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b1e1-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9b1e1-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9b1e1-139">End of server support</span></span><br/>    | <span data-ttu-id="9b1e1-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9b1e1-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9b1e1-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b1e1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b1e1-142"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b1e1-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b1e1-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9b1e1-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b1e1-144"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b1e1-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b1e1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b1e1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b1e1-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b1e1-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b1e1-147">IID</span><span class="sxs-lookup"><span data-stu-id="9b1e1-147">IID</span></span><br/>                      | <span data-ttu-id="9b1e1-148">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="9b1e1-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

