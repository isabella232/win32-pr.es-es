---
description: Recupera el byte del identificador de la instrucción de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'Método ISCardCmd:: get_InstructionId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003035"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="47030-103">ISCardCmd:: get \_ InstructionId (método)</span><span class="sxs-lookup"><span data-stu-id="47030-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="47030-104">\[El método **Get \_ InstructionId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="47030-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="47030-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47030-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47030-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="47030-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="47030-107">El método **Get \_ InstructionId** recupera el byte del identificador de instrucciones de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="47030-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="47030-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47030-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="47030-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47030-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47030-110">*pbyIns* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="47030-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47030-111">Puntero al byte que es el identificador de instrucción de las APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="47030-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47030-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47030-112">Return value</span></span>

<span data-ttu-id="47030-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="47030-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="47030-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="47030-114">Return code</span></span>                                                                                   | <span data-ttu-id="47030-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="47030-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="47030-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="47030-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47030-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="47030-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="47030-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47030-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="47030-119">El parámetro *pbyIns* no es válido.</span><span class="sxs-lookup"><span data-stu-id="47030-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="47030-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="47030-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="47030-121">Se pasó un puntero no válido en *pbyIns*.</span><span class="sxs-lookup"><span data-stu-id="47030-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="47030-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47030-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="47030-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="47030-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="47030-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47030-124">Remarks</span></span>

<span data-ttu-id="47030-125">Para establecer el identificador de instrucciones en un nuevo valor, llame a [**Put \_ InstructionId**](iscardcmd-put-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="47030-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="47030-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="47030-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="47030-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47030-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="47030-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="47030-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47030-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47030-129">Examples</span></span>

<span data-ttu-id="47030-130">En el ejemplo siguiente se muestra cómo recuperar el byte del identificador de instrucción de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="47030-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="47030-131">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="47030-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="47030-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47030-132">Requirements</span></span>



| <span data-ttu-id="47030-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="47030-133">Requirement</span></span> | <span data-ttu-id="47030-134">Value</span><span class="sxs-lookup"><span data-stu-id="47030-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47030-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47030-135">Minimum supported client</span></span><br/> | <span data-ttu-id="47030-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="47030-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="47030-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47030-137">Minimum supported server</span></span><br/> | <span data-ttu-id="47030-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="47030-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47030-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="47030-139">End of client support</span></span><br/>    | <span data-ttu-id="47030-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="47030-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="47030-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="47030-141">End of server support</span></span><br/>    | <span data-ttu-id="47030-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47030-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="47030-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47030-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="47030-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="47030-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="47030-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="47030-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="47030-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47030-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47030-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47030-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47030-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47030-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="47030-149">IID</span><span class="sxs-lookup"><span data-stu-id="47030-149">IID</span></span><br/>                      | <span data-ttu-id="47030-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="47030-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="47030-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="47030-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47030-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="47030-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="47030-153">**Put \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="47030-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
