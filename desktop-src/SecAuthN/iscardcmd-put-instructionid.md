---
description: Establece el identificador de instrucción determinado en la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: 'ISCardCmd: método de ut_InstructionId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001385"
---
# <a name="iscardcmdput_instructionid-method"></a><span data-ttu-id="73463-103">ISCardCmd::p \_ método InstructionId UT</span><span class="sxs-lookup"><span data-stu-id="73463-103">ISCardCmd::put\_InstructionId method</span></span>

<span data-ttu-id="73463-104">\[El método **Put \_ InstructionId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="73463-104">\[The **put\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="73463-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="73463-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="73463-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="73463-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="73463-107">El método **Put \_ InstructionId** establece el identificador de instrucción determinado en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="73463-107">The **put\_InstructionId** method sets the given instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="73463-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73463-108">Syntax</span></span>


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a><span data-ttu-id="73463-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73463-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73463-110">*byIns* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73463-110">*byIns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73463-111">Byte que es el identificador de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="73463-111">The byte that is the instruction identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73463-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73463-112">Return value</span></span>

<span data-ttu-id="73463-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="73463-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="73463-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="73463-114">Return code</span></span>                                                                                   | <span data-ttu-id="73463-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="73463-115">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="73463-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="73463-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="73463-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="73463-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="73463-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="73463-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="73463-119">El parámetro *byIns* no es válido.</span><span class="sxs-lookup"><span data-stu-id="73463-119">The *byIns* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="73463-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="73463-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="73463-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="73463-121">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="73463-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73463-122">Remarks</span></span>

<span data-ttu-id="73463-123">Para obtener el identificador de instrucción existente, llame a [**Get \_ InstructionId**](iscardcmd-get-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="73463-123">To get the existing instructional identifier, call [**get\_InstructionId**](iscardcmd-get-instructionid.md).</span></span>

<span data-ttu-id="73463-124">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="73463-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="73463-125">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73463-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="73463-126">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="73463-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="73463-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="73463-127">Examples</span></span>

<span data-ttu-id="73463-128">En el ejemplo siguiente se muestra cómo establecer un identificador de instrucción en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="73463-128">The following example shows how to set an instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="73463-129">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="73463-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="73463-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73463-130">Requirements</span></span>



| <span data-ttu-id="73463-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="73463-131">Requirement</span></span> | <span data-ttu-id="73463-132">Value</span><span class="sxs-lookup"><span data-stu-id="73463-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73463-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73463-133">Minimum supported client</span></span><br/> | <span data-ttu-id="73463-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="73463-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="73463-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73463-135">Minimum supported server</span></span><br/> | <span data-ttu-id="73463-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="73463-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73463-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="73463-137">End of client support</span></span><br/>    | <span data-ttu-id="73463-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="73463-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="73463-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="73463-139">End of server support</span></span><br/>    | <span data-ttu-id="73463-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="73463-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="73463-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73463-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="73463-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="73463-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="73463-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="73463-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="73463-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="73463-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="73463-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73463-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73463-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73463-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="73463-147">IID</span><span class="sxs-lookup"><span data-stu-id="73463-147">IID</span></span><br/>                      | <span data-ttu-id="73463-148">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="73463-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="73463-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="73463-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73463-150">**obtener \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="73463-150">**get\_InstructionId**</span></span>](iscardcmd-get-instructionid.md)
</dt> <dt>

[<span data-ttu-id="73463-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="73463-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
