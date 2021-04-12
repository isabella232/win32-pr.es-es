---
description: Construye una unidad de datos de protocolo de aplicación de comandos (APDU) válida para la transmisión a una tarjeta inteligente.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'ISCardCmd:: BuildCmd (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277974"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="d0267-103">ISCardCmd:: BuildCmd (método)</span><span class="sxs-lookup"><span data-stu-id="d0267-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="d0267-104">\[El método **BuildCmd** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d0267-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0267-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d0267-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0267-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d0267-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d0267-107">El método **BuildCmd** crea una [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de comandos (APDU) válida para la transmisión a una [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d0267-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0267-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0267-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="d0267-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0267-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0267-110">*byClassId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-111">Identificador de clase de comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d0267-112">*byInsId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-113">Identificador de instrucción de comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d0267-114">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-115">Primer parámetro del comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d0267-116">*byP2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-117">Segundo parámetro del comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d0267-118">*pbyData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-119">Puntero a la parte de datos del comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="d0267-120">*p1Le* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0267-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0267-121">Puntero a un entero largo que contiene la longitud esperada de los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="d0267-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0267-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0267-122">Return value</span></span>

<span data-ttu-id="d0267-123">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d0267-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d0267-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d0267-124">Return code</span></span>                                                                                   | <span data-ttu-id="d0267-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0267-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d0267-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0267-127">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d0267-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="d0267-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d0267-129">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0267-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="d0267-130"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d0267-131">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="d0267-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="d0267-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0267-133">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="d0267-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="d0267-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0267-134">Remarks</span></span>

<span data-ttu-id="d0267-135">Para encapsular el comando en otro comando, llame a [**Encapsulate**](iscardcmd-encapsulate.md).</span><span class="sxs-lookup"><span data-stu-id="d0267-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="d0267-136">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d0267-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d0267-137">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0267-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d0267-138">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d0267-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0267-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d0267-139">Examples</span></span>

<span data-ttu-id="d0267-140">En el ejemplo siguiente se muestra cómo construir una APDU de comando.</span><span class="sxs-lookup"><span data-stu-id="d0267-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="d0267-141">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) y que pIByteRequest es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) inicializada con una llamada anterior al método [**IByteBuffer:: Initialize**](ibytebuffer-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="d0267-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d0267-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0267-142">Requirements</span></span>



| <span data-ttu-id="d0267-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0267-143">Requirement</span></span> | <span data-ttu-id="d0267-144">Value</span><span class="sxs-lookup"><span data-stu-id="d0267-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0267-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0267-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d0267-146">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d0267-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0267-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0267-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d0267-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0267-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0267-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d0267-149">End of client support</span></span><br/>    | <span data-ttu-id="d0267-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0267-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d0267-151">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d0267-151">End of server support</span></span><br/>    | <span data-ttu-id="d0267-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0267-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d0267-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0267-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0267-154"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0267-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0267-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0267-156"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0267-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0267-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0267-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0267-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0267-159">IID</span><span class="sxs-lookup"><span data-stu-id="d0267-159">IID</span></span><br/>                      | <span data-ttu-id="d0267-160">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d0267-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d0267-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0267-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0267-162">**Encapsular**</span><span class="sxs-lookup"><span data-stu-id="d0267-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="d0267-163">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d0267-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
