---
description: Construye un comando APDU (unidad de datos de protocolo de aplicación) que establece secuencialmente parte del contenido de un archivo elemental en su estado borrado lógico, empezando por un desplazamiento determinado.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816:: EraseBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653013"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="8a389-103">ISCardISO7816:: EraseBinary (método)</span><span class="sxs-lookup"><span data-stu-id="8a389-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="8a389-104">\[El método **EraseBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8a389-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8a389-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8a389-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a389-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8a389-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8a389-107">El método **EraseBinary** crea un comando APDU ( [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) ) que establece secuencialmente parte del contenido de un archivo elemental en su estado borrado lógico, empezando por un desplazamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="8a389-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a389-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a389-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8a389-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a389-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a389-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a389-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a389-111">Posición RFU.</span><span class="sxs-lookup"><span data-stu-id="8a389-111">RFU position.</span></span>

<span data-ttu-id="8a389-112">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="8a389-113">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="8a389-114">Si el campo de datos está presente, codifica el desplazamiento de la primera unidad de datos que no se va a borrar.</span><span class="sxs-lookup"><span data-stu-id="8a389-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="8a389-115">Este desplazamiento será mayor que el que se codifica en P1-P2.</span><span class="sxs-lookup"><span data-stu-id="8a389-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="8a389-116">Cuando el campo de datos está vacío, el comando borra hasta el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8a389-117">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a389-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a389-118">Posición RFU.</span><span class="sxs-lookup"><span data-stu-id="8a389-118">RFU position.</span></span>

<span data-ttu-id="8a389-119">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="8a389-120">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se va a borrar (en unidades de datos) desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="8a389-121">Si el campo de datos está presente, codifica el desplazamiento de la primera unidad de datos que no se va a borrar.</span><span class="sxs-lookup"><span data-stu-id="8a389-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="8a389-122">Este desplazamiento será mayor que el que se codifica en P1-P2.</span><span class="sxs-lookup"><span data-stu-id="8a389-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="8a389-123">Cuando el campo de datos está vacío, el comando borra hasta el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="8a389-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8a389-124">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a389-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a389-125">Puntero a los datos que especifican el intervalo de borrado.</span><span class="sxs-lookup"><span data-stu-id="8a389-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="8a389-126">Este parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8a389-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a389-127">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8a389-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a389-128">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="8a389-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="8a389-129">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="8a389-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="8a389-130">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="8a389-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a389-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a389-131">Return value</span></span>

<span data-ttu-id="8a389-132">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="8a389-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8a389-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a389-133">Return code</span></span>                                                                                   | <span data-ttu-id="8a389-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a389-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="8a389-135"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a389-136">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a389-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="8a389-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8a389-138">Se pasó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="8a389-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="8a389-139"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a389-140">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="8a389-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="8a389-141"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a389-142">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="8a389-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="8a389-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a389-143">Remarks</span></span>

<span data-ttu-id="8a389-144">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="8a389-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="8a389-145">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="8a389-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="8a389-146">Los archivos elementales sin una estructura transparente no se pueden borrar.</span><span class="sxs-lookup"><span data-stu-id="8a389-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="8a389-147">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.</span><span class="sxs-lookup"><span data-stu-id="8a389-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="8a389-148">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="8a389-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="8a389-149">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a389-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8a389-150">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8a389-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a389-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a389-151">Requirements</span></span>



| <span data-ttu-id="8a389-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a389-152">Requirement</span></span> | <span data-ttu-id="8a389-153">Value</span><span class="sxs-lookup"><span data-stu-id="8a389-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a389-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a389-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8a389-155">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8a389-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8a389-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a389-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8a389-157">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a389-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a389-158">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8a389-158">End of client support</span></span><br/>    | <span data-ttu-id="8a389-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a389-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8a389-160">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8a389-160">End of server support</span></span><br/>    | <span data-ttu-id="8a389-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a389-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8a389-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a389-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a389-163"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a389-164">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a389-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a389-165"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a389-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a389-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a389-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a389-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a389-168">IID</span><span class="sxs-lookup"><span data-stu-id="8a389-168">IID</span></span><br/>                      | <span data-ttu-id="8a389-169">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8a389-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8a389-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a389-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a389-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8a389-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="8a389-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="8a389-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="8a389-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="8a389-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="8a389-174">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="8a389-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
