---
description: Recupera el identificador de clase de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Método ISCardCmd:: get_ClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154360"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="4b72e-103">ISCardCmd:: get \_ ClassID (método)</span><span class="sxs-lookup"><span data-stu-id="4b72e-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="4b72e-104">\[El método **Get \_ ClassID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4b72e-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b72e-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4b72e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b72e-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="4b72e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4b72e-107">El método **Get \_ ClassID** recupera el identificador de clase de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4b72e-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b72e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b72e-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="4b72e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b72e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b72e-110">*pbyClass* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b72e-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b72e-111">Puntero al byte que representa el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="4b72e-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b72e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b72e-112">Return value</span></span>

<span data-ttu-id="4b72e-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4b72e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4b72e-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4b72e-114">Return code</span></span>                                                                                   | <span data-ttu-id="4b72e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b72e-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4b72e-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4b72e-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="4b72e-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="4b72e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4b72e-119">El parámetro *pbyClass* no es válido.</span><span class="sxs-lookup"><span data-stu-id="4b72e-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4b72e-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4b72e-121">Se pasó un puntero no válido en *pbyClass*.</span><span class="sxs-lookup"><span data-stu-id="4b72e-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="4b72e-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4b72e-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="4b72e-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="4b72e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b72e-124">Remarks</span></span>

<span data-ttu-id="4b72e-125">Para establecer el identificador de clase en un nuevo valor, llame a [**Put \_ ClassID**](iscardcmd-put-classid.md).</span><span class="sxs-lookup"><span data-stu-id="4b72e-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="4b72e-126">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4b72e-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4b72e-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b72e-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4b72e-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4b72e-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4b72e-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4b72e-129">Examples</span></span>

<span data-ttu-id="4b72e-130">En el ejemplo siguiente se muestra cómo recuperar el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="4b72e-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="4b72e-131">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4b72e-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4b72e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b72e-132">Requirements</span></span>



| <span data-ttu-id="4b72e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b72e-133">Requirement</span></span> | <span data-ttu-id="4b72e-134">Value</span><span class="sxs-lookup"><span data-stu-id="4b72e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b72e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b72e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4b72e-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4b72e-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b72e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b72e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4b72e-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b72e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b72e-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4b72e-139">End of client support</span></span><br/>    | <span data-ttu-id="4b72e-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b72e-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4b72e-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4b72e-141">End of server support</span></span><br/>    | <span data-ttu-id="4b72e-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b72e-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4b72e-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b72e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b72e-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b72e-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4b72e-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b72e-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b72e-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b72e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b72e-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b72e-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b72e-149">IID</span><span class="sxs-lookup"><span data-stu-id="4b72e-149">IID</span></span><br/>                      | <span data-ttu-id="4b72e-150">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4b72e-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4b72e-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b72e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b72e-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4b72e-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4b72e-153">**Put \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="4b72e-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
