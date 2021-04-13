---
description: 'El método Revert descarta todos los cambios realizados en una secuencia de transacción desde la última llamada a IByteBuffer:: commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Método IByteBuffer:: revert (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275336"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="56908-103">IByteBuffer:: revert (método)</span><span class="sxs-lookup"><span data-stu-id="56908-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="56908-104">\[El método **Revert** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="56908-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56908-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56908-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="56908-106">La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="56908-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="56908-107">El método **Revert** descarta todos los cambios realizados en una secuencia de transacción desde la última llamada a [**IByteBuffer:: commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="56908-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="56908-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56908-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="56908-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56908-109">Parameters</span></span>

<span data-ttu-id="56908-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="56908-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56908-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56908-111">Return value</span></span>

<span data-ttu-id="56908-112">El valor devuelto es **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="56908-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="56908-113">Un valor de S \_ correcto indica que la llamada se realizó correctamente y que la secuencia se revirtió a su versión anterior.</span><span class="sxs-lookup"><span data-stu-id="56908-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="56908-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56908-114">Remarks</span></span>

<span data-ttu-id="56908-115">Este método descarta los cambios realizados en una secuencia de transacción desde la última operación de confirmación.</span><span class="sxs-lookup"><span data-stu-id="56908-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="56908-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56908-116">Examples</span></span>

<span data-ttu-id="56908-117">En el ejemplo siguiente se muestra la reversión de un flujo de transacción a la última operación confirmada.</span><span class="sxs-lookup"><span data-stu-id="56908-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="56908-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56908-118">Requirements</span></span>



| <span data-ttu-id="56908-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="56908-119">Requirement</span></span> | <span data-ttu-id="56908-120">Value</span><span class="sxs-lookup"><span data-stu-id="56908-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56908-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56908-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56908-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="56908-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56908-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56908-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56908-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56908-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56908-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="56908-125">End of client support</span></span><br/>    | <span data-ttu-id="56908-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="56908-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="56908-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="56908-127">End of server support</span></span><br/>    | <span data-ttu-id="56908-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56908-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="56908-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56908-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="56908-130"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56908-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56908-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="56908-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="56908-132"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56908-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56908-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56908-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56908-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56908-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="56908-135">IID</span><span class="sxs-lookup"><span data-stu-id="56908-135">IID</span></span><br/>                      | <span data-ttu-id="56908-136">IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="56908-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

