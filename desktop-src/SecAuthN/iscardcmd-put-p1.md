---
description: Establece el primer parámetro (P1) byte de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'ISCardCmd: método de ut_P1 de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648505"
---
# <a name="iscardcmdput_p1-method"></a><span data-ttu-id="6ee22-103">ISCardCmd::p \_ método UT P1</span><span class="sxs-lookup"><span data-stu-id="6ee22-103">ISCardCmd::put\_P1 method</span></span>

<span data-ttu-id="6ee22-104">\[El método **Put \_ P1** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6ee22-104">\[The **put\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ee22-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6ee22-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6ee22-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6ee22-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6ee22-107">El método **Put \_ P1** establece el primer parámetro (P1) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="6ee22-107">The **put\_P1** method sets the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee22-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ee22-108">Syntax</span></span>


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a><span data-ttu-id="6ee22-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ee22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee22-110">*byP1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ee22-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee22-111">Byte que es el campo P1.</span><span class="sxs-lookup"><span data-stu-id="6ee22-111">The byte that is the P1 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee22-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ee22-112">Return value</span></span>

<span data-ttu-id="6ee22-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6ee22-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6ee22-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6ee22-114">Return code</span></span>                                                                                   | <span data-ttu-id="6ee22-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ee22-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="6ee22-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6ee22-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ee22-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="6ee22-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6ee22-119">El parámetro *byP1* no es válido.</span><span class="sxs-lookup"><span data-stu-id="6ee22-119">The *byP1* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6ee22-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6ee22-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6ee22-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6ee22-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ee22-122">Remarks</span></span>

<span data-ttu-id="6ee22-123">Para establecer el valor P2 de APDU, llame a [**Get \_ P2**](iscardcmd-get-p2.md).</span><span class="sxs-lookup"><span data-stu-id="6ee22-123">To set the P2 value of the APDU, call [**get\_P2**](iscardcmd-get-p2.md).</span></span>

<span data-ttu-id="6ee22-124">Para recuperar los valores P1, P2 y P3 existentes, llame a [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) u [**Get \_ P3**](iscardcmd-get-p3.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6ee22-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="6ee22-125">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="6ee22-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="6ee22-126">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ee22-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6ee22-127">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6ee22-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6ee22-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ee22-128">Examples</span></span>

<span data-ttu-id="6ee22-129">En el ejemplo siguiente se muestra cómo establecer el primer parámetro (P1) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="6ee22-129">The following example shows how to set the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="6ee22-130">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="6ee22-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6ee22-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ee22-131">Requirements</span></span>



| <span data-ttu-id="6ee22-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee22-132">Requirement</span></span> | <span data-ttu-id="6ee22-133">Value</span><span class="sxs-lookup"><span data-stu-id="6ee22-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee22-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee22-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6ee22-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ee22-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ee22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee22-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ee22-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ee22-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6ee22-138">End of client support</span></span><br/>    | <span data-ttu-id="6ee22-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ee22-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6ee22-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6ee22-140">End of server support</span></span><br/>    | <span data-ttu-id="6ee22-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ee22-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6ee22-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ee22-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ee22-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ee22-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ee22-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ee22-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ee22-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ee22-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee22-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee22-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ee22-148">IID</span><span class="sxs-lookup"><span data-stu-id="6ee22-148">IID</span></span><br/>                      | <span data-ttu-id="6ee22-149">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6ee22-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6ee22-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ee22-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee22-151">**obtener \_ P1**</span><span class="sxs-lookup"><span data-stu-id="6ee22-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="6ee22-152">**obtener \_ P2**</span><span class="sxs-lookup"><span data-stu-id="6ee22-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="6ee22-153">**obtener \_ P3**</span><span class="sxs-lookup"><span data-stu-id="6ee22-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="6ee22-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="6ee22-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="6ee22-155">**Put \_ P2**</span><span class="sxs-lookup"><span data-stu-id="6ee22-155">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
