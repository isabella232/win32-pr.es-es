---
description: El método Item del objeto SWbemObjectSet obtiene un SWbemObject de la colección.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Método SWbemObjectSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706042"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="f8625-103">SWbemObjectSet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="f8625-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="f8625-104">El método **Item** del objeto [**SWbemObjectSet**](swbemobjectset.md) obtiene un [**SWbemObject**](swbemobject.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="f8625-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="f8625-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f8625-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8625-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8625-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="f8625-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8625-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8625-108">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="f8625-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="f8625-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8625-109">Required.</span></span> <span data-ttu-id="f8625-110">Ruta de acceso relativa del objeto que se va a recuperar de la colección.</span><span class="sxs-lookup"><span data-stu-id="f8625-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="f8625-111">Ejemplo: Win32 \_ LogicalDisk = "C:"</span><span class="sxs-lookup"><span data-stu-id="f8625-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8625-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8625-112">Return value</span></span>

<span data-ttu-id="f8625-113">Si se realiza correctamente, el objeto [**SWbemObject**](swbemobject.md) solicitado devuelve.</span><span class="sxs-lookup"><span data-stu-id="f8625-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8625-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f8625-114">Error codes</span></span>

<span data-ttu-id="f8625-115">Una vez finalizado el método **Item** , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="f8625-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="f8625-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f8625-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f8625-117">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f8625-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f8625-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f8625-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f8625-119">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="f8625-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f8625-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f8625-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f8625-121">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="f8625-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8625-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f8625-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f8625-123">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="f8625-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8625-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8625-124">Remarks</span></span>

<span data-ttu-id="f8625-125">El método **Item** puede requerir mucho tiempo de procesador porque el proveedor de los elementos del conjunto necesita una enumeración completa para devolver el resultado.</span><span class="sxs-lookup"><span data-stu-id="f8625-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8625-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8625-126">Requirements</span></span>



| <span data-ttu-id="f8625-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8625-127">Requirement</span></span> | <span data-ttu-id="f8625-128">Value</span><span class="sxs-lookup"><span data-stu-id="f8625-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8625-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8625-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8625-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8625-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8625-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8625-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8625-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8625-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8625-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8625-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8625-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8625-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8625-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f8625-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8625-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f8625-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f8625-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8625-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8625-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8625-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f8625-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="f8625-139">CLSID</span></span><br/>                    | <span data-ttu-id="f8625-140">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8625-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="f8625-141">IID</span><span class="sxs-lookup"><span data-stu-id="f8625-141">IID</span></span><br/>                      | <span data-ttu-id="f8625-142">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="f8625-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




