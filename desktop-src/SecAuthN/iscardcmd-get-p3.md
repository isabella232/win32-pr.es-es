---
description: Recupera el tercer parámetro (P3) byte de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Método ISCardCmd:: get_P3 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154357"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="7c43d-103">ISCardCmd:: get \_ P3 (método)</span><span class="sxs-lookup"><span data-stu-id="7c43d-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="7c43d-104">\[El método **Get \_ P3** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7c43d-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7c43d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c43d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c43d-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7c43d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7c43d-107">El método **Get \_ P3** recupera el tercer parámetro (P3) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="7c43d-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7c43d-108">Este valor de byte de solo lectura representa el tamaño de la parte de datos de APDU.</span><span class="sxs-lookup"><span data-stu-id="7c43d-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c43d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c43d-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="7c43d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c43d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c43d-111">*pbyP3* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7c43d-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c43d-112">Puntero al byte que es P3 desde las APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="7c43d-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c43d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c43d-113">Return value</span></span>

<span data-ttu-id="7c43d-114">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7c43d-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7c43d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7c43d-115">Return code</span></span>                                                                                   | <span data-ttu-id="7c43d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c43d-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7c43d-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7c43d-118">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c43d-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="7c43d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7c43d-120">*PbyP3* no es válido.</span><span class="sxs-lookup"><span data-stu-id="7c43d-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="7c43d-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7c43d-122">Se pasó un puntero no válido en *pbyP3*.</span><span class="sxs-lookup"><span data-stu-id="7c43d-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="7c43d-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7c43d-124">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7c43d-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="7c43d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c43d-125">Remarks</span></span>

<span data-ttu-id="7c43d-126">El parámetro P3 es de solo lectura y, por lo tanto, no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="7c43d-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="7c43d-127">Para obtener los parámetros P1 o P2, llame a [**Get \_ P1**](iscardcmd-get-p1.md) y [**Get \_ P2**](iscardcmd-get-p2.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7c43d-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="7c43d-128">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7c43d-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7c43d-129">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c43d-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7c43d-130">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7c43d-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7c43d-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c43d-131">Examples</span></span>

<span data-ttu-id="7c43d-132">En el ejemplo siguiente se muestra cómo recuperar el tercer parámetro (P3) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="7c43d-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7c43d-133">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7c43d-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7c43d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c43d-134">Requirements</span></span>



| <span data-ttu-id="7c43d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c43d-135">Requirement</span></span> | <span data-ttu-id="7c43d-136">Value</span><span class="sxs-lookup"><span data-stu-id="7c43d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c43d-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c43d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7c43d-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7c43d-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c43d-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c43d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7c43d-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c43d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c43d-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7c43d-141">End of client support</span></span><br/>    | <span data-ttu-id="7c43d-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c43d-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7c43d-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7c43d-143">End of server support</span></span><br/>    | <span data-ttu-id="7c43d-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c43d-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7c43d-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c43d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c43d-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c43d-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7c43d-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c43d-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c43d-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c43d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c43d-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c43d-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c43d-151">IID</span><span class="sxs-lookup"><span data-stu-id="7c43d-151">IID</span></span><br/>                      | <span data-ttu-id="7c43d-152">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7c43d-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7c43d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c43d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c43d-154">**obtener \_ P1**</span><span class="sxs-lookup"><span data-stu-id="7c43d-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="7c43d-155">**obtener \_ P2**</span><span class="sxs-lookup"><span data-stu-id="7c43d-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="7c43d-156">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="7c43d-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
