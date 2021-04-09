---
description: El método Close cierra el archivo especificado. No se permite más acceso al archivo.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'ISCardFileAccess:: Close (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154348"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="2042f-104">ISCardFileAccess:: Close (método)</span><span class="sxs-lookup"><span data-stu-id="2042f-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="2042f-105">\[El método **Close** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2042f-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2042f-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2042f-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2042f-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2042f-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2042f-108">El método **Close** cierra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2042f-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="2042f-109">No se permite más acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="2042f-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2042f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2042f-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="2042f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2042f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2042f-112">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2042f-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2042f-113">Identificador del archivo que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="2042f-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2042f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2042f-114">Return value</span></span>

<span data-ttu-id="2042f-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2042f-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2042f-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2042f-116">Return code</span></span>                                                                                   | <span data-ttu-id="2042f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2042f-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2042f-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2042f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2042f-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2042f-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2042f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2042f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2042f-121">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="2042f-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2042f-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2042f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2042f-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="2042f-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2042f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2042f-124">Remarks</span></span>

<span data-ttu-id="2042f-125">Para abrir un archivo, llame a [**Open**](iscardfileaccess-open.md).</span><span class="sxs-lookup"><span data-stu-id="2042f-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="2042f-126">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2042f-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="2042f-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2042f-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2042f-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2042f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2042f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2042f-129">Requirements</span></span>



| <span data-ttu-id="2042f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2042f-130">Requirement</span></span> | <span data-ttu-id="2042f-131">Value</span><span class="sxs-lookup"><span data-stu-id="2042f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2042f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2042f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2042f-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2042f-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2042f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2042f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2042f-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2042f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2042f-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2042f-136">End of client support</span></span><br/>    | <span data-ttu-id="2042f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2042f-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2042f-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2042f-138">End of server support</span></span><br/>    | <span data-ttu-id="2042f-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2042f-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2042f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2042f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2042f-141">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="2042f-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="2042f-142">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="2042f-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
