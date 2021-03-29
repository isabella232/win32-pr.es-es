---
description: El método ReadBinary crea un comando de unidad de datos de protocolo de aplicación (APDU) que adquiere un mensaje de respuesta que proporciona la parte del contenido de un archivo elemental estructurado de forma transparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816:: ReadBinary (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912465"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="55b10-103">ISCardISO7816:: ReadBinary (método)</span><span class="sxs-lookup"><span data-stu-id="55b10-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="55b10-104">\[El método **ReadBinary** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="55b10-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55b10-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="55b10-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55b10-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="55b10-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="55b10-107">El método **ReadBinary** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que adquiere un mensaje de respuesta que proporciona la parte del contenido de un archivo elemental estructurado de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="55b10-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55b10-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="55b10-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55b10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b10-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55b10-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b10-111">El campo P1-P2, desplazado hasta el primer byte que se va a leer desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="55b10-112">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a leer en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="55b10-113">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se leerá en unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="55b10-114">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55b10-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b10-115">El campo P1-P2, desplazado hasta el primer byte que se va a leer desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="55b10-116">Si B8 = 1 en P1, B7 y B6 de P1 se establecen en cero (RFU bits), B5 en B1 de P1 son un identificador de EF corto y P2 es el desplazamiento del primer byte que se va a leer en las unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="55b10-117">Si B8 = 0 en P1, P1 \| \| P2 es el desplazamiento del primer byte que se leerá en unidades de datos desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="55b10-118">*lBytesToRead* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55b10-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b10-119">Número de bytes que se van a leer del EF transparente.</span><span class="sxs-lookup"><span data-stu-id="55b10-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="55b10-120">Si el campo le contiene solo ceros, dentro del límite de 256 para la longitud corta o 65536 para la longitud extendida, se deben leer todos los bytes hasta el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="55b10-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="55b10-121">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="55b10-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55b10-122">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="55b10-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="55b10-123">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="55b10-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="55b10-124">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="55b10-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b10-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55b10-125">Return value</span></span>

<span data-ttu-id="55b10-126">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="55b10-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="55b10-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="55b10-127">Return code</span></span>                                                                                   | <span data-ttu-id="55b10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="55b10-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="55b10-129"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="55b10-130">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="55b10-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="55b10-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="55b10-132">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="55b10-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="55b10-133"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="55b10-134">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="55b10-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="55b10-135"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="55b10-136">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="55b10-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="55b10-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55b10-137">Remarks</span></span>

<span data-ttu-id="55b10-138">El comando encapsulado solo puede realizarse si el estado de seguridad de la [*tarjeta inteligente*](../secgloss/s-gly.md) cumple los atributos de seguridad del archivo elemental que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="55b10-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="55b10-139">Cuando el comando contiene un identificador elemental básico válido, establece el archivo como archivo elemental actual.</span><span class="sxs-lookup"><span data-stu-id="55b10-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="55b10-140">Los archivos elementales sin una estructura transparente no se pueden borrar.</span><span class="sxs-lookup"><span data-stu-id="55b10-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="55b10-141">El comando encapsulado se anula si se aplica a un archivo elemental sin una estructura transparente.</span><span class="sxs-lookup"><span data-stu-id="55b10-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="55b10-142">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="55b10-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="55b10-143">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55b10-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="55b10-144">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="55b10-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55b10-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b10-145">Requirements</span></span>



| <span data-ttu-id="55b10-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b10-146">Requirement</span></span> | <span data-ttu-id="55b10-147">Value</span><span class="sxs-lookup"><span data-stu-id="55b10-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b10-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55b10-148">Minimum supported client</span></span><br/> | <span data-ttu-id="55b10-149">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="55b10-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55b10-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55b10-150">Minimum supported server</span></span><br/> | <span data-ttu-id="55b10-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="55b10-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55b10-152">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="55b10-152">End of client support</span></span><br/>    | <span data-ttu-id="55b10-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="55b10-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="55b10-154">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="55b10-154">End of server support</span></span><br/>    | <span data-ttu-id="55b10-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55b10-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="55b10-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55b10-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b10-157"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55b10-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="55b10-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="55b10-159"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55b10-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55b10-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b10-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b10-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55b10-162">IID</span><span class="sxs-lookup"><span data-stu-id="55b10-162">IID</span></span><br/>                      | <span data-ttu-id="55b10-163">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="55b10-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="55b10-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="55b10-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b10-165">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="55b10-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="55b10-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="55b10-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="55b10-167">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="55b10-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="55b10-168">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="55b10-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
