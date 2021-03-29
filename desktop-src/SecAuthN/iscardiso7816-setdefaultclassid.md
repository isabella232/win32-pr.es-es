---
description: El método SetDefaultClassId asigna un byte de identificador de clase estándar que se usará en todas las operaciones al construir una unidad de datos de protocolo de aplicación de comandos (APDU) ISO 7816-4. De forma predeterminada, el identificador de clase estándar byte es 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816:: SetDefaultClassId (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648460"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="a4449-104">ISCardISO7816:: SetDefaultClassId (método)</span><span class="sxs-lookup"><span data-stu-id="a4449-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="a4449-105">\[El método **SetDefaultClassId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4449-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4449-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a4449-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4449-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a4449-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a4449-108">El método **SetDefaultClassId** asigna un byte de identificador de clase estándar que se usará en todas las operaciones al construir una [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de comandos (APDU) ISO 7816-4.</span><span class="sxs-lookup"><span data-stu-id="a4449-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a4449-109">De forma predeterminada, el identificador de clase estándar byte es 0x00.</span><span class="sxs-lookup"><span data-stu-id="a4449-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4449-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4449-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="a4449-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4449-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4449-112">*byClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4449-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4449-113">Byte de ID. de clase.</span><span class="sxs-lookup"><span data-stu-id="a4449-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4449-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4449-114">Return value</span></span>

<span data-ttu-id="a4449-115">Los posibles valores devueltos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a4449-115">The possible return values are the following:</span></span>



| <span data-ttu-id="a4449-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a4449-116">Return code</span></span>                                                                          | <span data-ttu-id="a4449-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4449-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a4449-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a4449-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a4449-119">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4449-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="a4449-120">Para obtener una lista de todos los métodos proporcionados por la interfaz [**ISCardISO7816**](iscardiso7816.md) , vea **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="a4449-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="a4449-121">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4449-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a4449-122">Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a4449-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4449-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4449-123">Requirements</span></span>



| <span data-ttu-id="a4449-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4449-124">Requirement</span></span> | <span data-ttu-id="a4449-125">Value</span><span class="sxs-lookup"><span data-stu-id="a4449-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4449-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4449-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4449-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a4449-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a4449-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4449-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4449-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4449-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4449-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a4449-130">End of client support</span></span><br/>    | <span data-ttu-id="a4449-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4449-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a4449-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a4449-132">End of server support</span></span><br/>    | <span data-ttu-id="a4449-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4449-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a4449-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4449-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4449-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4449-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4449-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a4449-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4449-137"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4449-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4449-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a4449-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4449-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4449-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a4449-140">IID</span><span class="sxs-lookup"><span data-stu-id="a4449-140">IID</span></span><br/>                      | <span data-ttu-id="a4449-141">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a4449-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a4449-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4449-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4449-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a4449-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
