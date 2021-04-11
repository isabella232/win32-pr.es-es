---
description: El método Clear borra los búferes de la unidad de datos de protocolo de aplicación (APDU) y del mensaje APDU de respuesta.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'ISCardCmd:: CLEAR (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154364"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="7c884-103">ISCardCmd:: CLEAR (método)</span><span class="sxs-lookup"><span data-stu-id="7c884-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="7c884-104">\[El método **Clear** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7c884-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7c884-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c884-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c884-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7c884-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7c884-107">El método **Clear** borra los búferes de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) y del mensaje APDU de [*respuesta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7c884-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c884-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c884-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="7c884-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c884-109">Parameters</span></span>

<span data-ttu-id="7c884-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c884-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c884-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c884-111">Return value</span></span>

<span data-ttu-id="7c884-112">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7c884-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7c884-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7c884-113">Return code</span></span>                                                                             | <span data-ttu-id="7c884-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c884-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7c884-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7c884-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c884-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7c884-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7c884-118">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="7c884-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7c884-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c884-119">Remarks</span></span>

<span data-ttu-id="7c884-120">Para compilar una APDU de comando, llame a [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7c884-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="7c884-121">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7c884-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7c884-122">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c884-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7c884-123">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7c884-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7c884-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c884-124">Examples</span></span>

<span data-ttu-id="7c884-125">En el ejemplo siguiente se muestra cómo borrar los búferes de mensajes APDU y reply APDU.</span><span class="sxs-lookup"><span data-stu-id="7c884-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7c884-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c884-126">Requirements</span></span>



| <span data-ttu-id="7c884-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c884-127">Requirement</span></span> | <span data-ttu-id="7c884-128">Value</span><span class="sxs-lookup"><span data-stu-id="7c884-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c884-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c884-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7c884-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7c884-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c884-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c884-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7c884-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c884-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c884-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7c884-133">End of client support</span></span><br/>    | <span data-ttu-id="7c884-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c884-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7c884-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7c884-135">End of server support</span></span><br/>    | <span data-ttu-id="7c884-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c884-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7c884-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c884-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c884-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c884-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7c884-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c884-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c884-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c884-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c884-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c884-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c884-143">IID</span><span class="sxs-lookup"><span data-stu-id="7c884-143">IID</span></span><br/>                      | <span data-ttu-id="7c884-144">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7c884-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7c884-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c884-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c884-146">**ISCardCmd::BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="7c884-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="7c884-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="7c884-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
