---
description: El método STAT recupera información estadística del objeto de secuencia.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'IByteBuffer:: Stat (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652987"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="4e075-103">IByteBuffer:: Stat (método)</span><span class="sxs-lookup"><span data-stu-id="4e075-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="4e075-104">\[El método **STAT** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4e075-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4e075-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e075-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4e075-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4e075-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4e075-107">El método **STAT** recupera información estadística del objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="4e075-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e075-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e075-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="4e075-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e075-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e075-110">*pstatstg* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e075-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e075-111">Apunta a una estructura **STATSTRUCT** donde este método coloca información sobre este objeto de flujo.</span><span class="sxs-lookup"><span data-stu-id="4e075-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="4e075-112">Este puntero es **null** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="4e075-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="4e075-113">*grfStatFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e075-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e075-114">Especifica que este método no devuelve algunos de los campos de la estructura **STATSTRUCT** , con lo que se guarda una operación de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e075-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="4e075-115">Los valores se toman de la enumeración [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)</span><span class="sxs-lookup"><span data-stu-id="4e075-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e075-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e075-116">Return value</span></span>

<span data-ttu-id="4e075-117">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4e075-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4e075-118">Un valor de S \_ correcto indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e075-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e075-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e075-119">Remarks</span></span>

<span data-ttu-id="4e075-120">El método **IByteBuffer:: Stat** recupera un puntero a la estructura **STATSTRUCT** que contiene información sobre esta secuencia abierta.</span><span class="sxs-lookup"><span data-stu-id="4e075-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="4e075-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e075-121">Examples</span></span>

<span data-ttu-id="4e075-122">En el ejemplo siguiente se muestra cómo recuperar información estadística de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4e075-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="4e075-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e075-123">Requirements</span></span>



| <span data-ttu-id="4e075-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e075-124">Requirement</span></span> | <span data-ttu-id="4e075-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e075-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e075-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e075-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4e075-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4e075-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e075-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e075-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4e075-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e075-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e075-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4e075-130">End of client support</span></span><br/>    | <span data-ttu-id="4e075-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e075-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4e075-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4e075-132">End of server support</span></span><br/>    | <span data-ttu-id="4e075-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e075-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4e075-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e075-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e075-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e075-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e075-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4e075-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e075-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e075-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e075-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e075-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e075-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e075-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e075-140">IID</span><span class="sxs-lookup"><span data-stu-id="4e075-140">IID</span></span><br/>                      | <span data-ttu-id="4e075-141">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4e075-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

