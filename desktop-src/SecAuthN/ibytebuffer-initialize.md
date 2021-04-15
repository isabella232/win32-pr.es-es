---
description: El método Initialize prepara el objeto IByteBuffer para su uso. Se debe llamar a este método antes de llamar a otros métodos de la interfaz IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'IByteBuffer:: Initialize (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649187"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="de888-104">IByteBuffer:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="de888-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="de888-105">\[El método **Initialize** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="de888-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="de888-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="de888-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="de888-107">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="de888-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="de888-108">El método **Initialize** prepara el objeto [**IByteBuffer**](ibytebuffer.md) para su uso.</span><span class="sxs-lookup"><span data-stu-id="de888-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="de888-109">Se debe llamar a este método antes de llamar a otros métodos de la interfaz **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="de888-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="de888-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de888-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="de888-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de888-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de888-112">*Lsize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de888-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de888-113">Tamaño inicial, en bytes, de los datos que va a contener la secuencia.</span><span class="sxs-lookup"><span data-stu-id="de888-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="de888-114">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de888-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de888-115">Si no **es null**, los datos iniciales que se van a escribir en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="de888-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de888-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de888-116">Return value</span></span>

<span data-ttu-id="de888-117">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="de888-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="de888-118">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="de888-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="de888-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de888-119">Remarks</span></span>

<span data-ttu-id="de888-120">Al utilizar una nueva secuencia [**IByteBuffer**](ibytebuffer.md) , llame a este método antes de usar cualquiera de los otros métodos **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="de888-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="de888-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="de888-121">Examples</span></span>

<span data-ttu-id="de888-122">En el ejemplo siguiente se muestra cómo inicializar el objeto [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="de888-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="de888-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de888-123">Requirements</span></span>



| <span data-ttu-id="de888-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="de888-124">Requirement</span></span> | <span data-ttu-id="de888-125">Value</span><span class="sxs-lookup"><span data-stu-id="de888-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de888-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de888-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de888-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="de888-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de888-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de888-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de888-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="de888-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de888-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="de888-130">End of client support</span></span><br/>    | <span data-ttu-id="de888-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="de888-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="de888-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="de888-132">End of server support</span></span><br/>    | <span data-ttu-id="de888-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de888-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="de888-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de888-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="de888-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de888-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de888-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de888-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="de888-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de888-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de888-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de888-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de888-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de888-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="de888-140">IID</span><span class="sxs-lookup"><span data-stu-id="de888-140">IID</span></span><br/>                      | <span data-ttu-id="de888-141">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="de888-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

