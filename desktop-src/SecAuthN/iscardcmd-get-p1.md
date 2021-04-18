---
description: Recupera el primer parámetro (P1) byte de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'Método ISCardCmd:: get_P1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541830"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="2dcc4-103">ISCardCmd:: get \_ P1 (método)</span><span class="sxs-lookup"><span data-stu-id="2dcc4-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="2dcc4-104">\[El método **Get \_ P1** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2dcc4-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2dcc4-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2dcc4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2dcc4-107">El método **Get \_ P1** recupera el primer parámetro (P1) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="2dcc4-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dcc4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dcc4-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="2dcc4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dcc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dcc4-110">*pbyP1* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2dcc4-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dcc4-111">Puntero al byte P1 en APDU en la devolución.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dcc4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dcc4-112">Return value</span></span>

<span data-ttu-id="2dcc4-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2dcc4-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2dcc4-114">Return code</span></span>                                                                                   | <span data-ttu-id="2dcc4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2dcc4-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2dcc4-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2dcc4-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="2dcc4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2dcc4-119">El parámetro *pbyP1* no es válido.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="2dcc4-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2dcc4-121">Se pasó un puntero no válido en *pbyP1*.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="2dcc4-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2dcc4-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="2dcc4-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="2dcc4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dcc4-124">Remarks</span></span>

<span data-ttu-id="2dcc4-125">Para establecer el parámetro P1 en un nuevo valor, llame a [**Put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc4-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="2dcc4-126">Para obtener los parámetros P2 o P3, llame a [**Get \_ P2**](iscardcmd-get-p2.md) y [**Get \_ P3**](iscardcmd-get-p3.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="2dcc4-127">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc4-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="2dcc4-128">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2dcc4-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2dcc4-129">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2dcc4-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2dcc4-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2dcc4-130">Examples</span></span>

<span data-ttu-id="2dcc4-131">En el ejemplo siguiente se muestra cómo recuperar el primer parámetro (P1) byte de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="2dcc4-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="2dcc4-132">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="2dcc4-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2dcc4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dcc4-133">Requirements</span></span>



| <span data-ttu-id="2dcc4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dcc4-134">Requirement</span></span> | <span data-ttu-id="2dcc4-135">Value</span><span class="sxs-lookup"><span data-stu-id="2dcc4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dcc4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dcc4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2dcc4-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2dcc4-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2dcc4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dcc4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2dcc4-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dcc4-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2dcc4-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2dcc4-140">End of client support</span></span><br/>    | <span data-ttu-id="2dcc4-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2dcc4-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2dcc4-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2dcc4-142">End of server support</span></span><br/>    | <span data-ttu-id="2dcc4-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2dcc4-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2dcc4-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dcc4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dcc4-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dcc4-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2dcc4-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="2dcc4-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2dcc4-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2dcc4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dcc4-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dcc4-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2dcc4-150">IID</span><span class="sxs-lookup"><span data-stu-id="2dcc4-150">IID</span></span><br/>                      | <span data-ttu-id="2dcc4-151">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2dcc4-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2dcc4-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dcc4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dcc4-153">**obtener \_ P2**</span><span class="sxs-lookup"><span data-stu-id="2dcc4-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="2dcc4-154">**obtener \_ P3**</span><span class="sxs-lookup"><span data-stu-id="2dcc4-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="2dcc4-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="2dcc4-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="2dcc4-156">**Put \_ P1**</span><span class="sxs-lookup"><span data-stu-id="2dcc4-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
