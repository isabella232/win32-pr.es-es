---
description: Especifica la dirección de nodo (NAD) que se va a usar con la interfaz ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: método de ut_Nad de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908298"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="784a5-103">ISCardCmd: \_ método Nad:p UT</span><span class="sxs-lookup"><span data-stu-id="784a5-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="784a5-104">\[El método **Put \_ nad** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="784a5-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="784a5-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="784a5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="784a5-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="784a5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="784a5-107">El método de **colocación del \_ nad** especifica la dirección del nodo (NAD) que se va a usar con la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="784a5-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="784a5-108">Esto se aplica a las comunicaciones que usan solo las comunicaciones de [*Protocolo T = 1*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="784a5-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="784a5-109">De forma predeterminada, el objeto [**ISCardCmd**](iscardcmd.md) usa un nad de cero.</span><span class="sxs-lookup"><span data-stu-id="784a5-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="784a5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="784a5-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="784a5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="784a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784a5-112">*bNad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="784a5-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="784a5-113">Byte que representa el NAD que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="784a5-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="784a5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="784a5-114">Return value</span></span>

<span data-ttu-id="784a5-115">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="784a5-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="784a5-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="784a5-116">Return code</span></span>                                                                                  | <span data-ttu-id="784a5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="784a5-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="784a5-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="784a5-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="784a5-119">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="784a5-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="784a5-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="784a5-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="784a5-121">El parámetro *bNad* no es válido.</span><span class="sxs-lookup"><span data-stu-id="784a5-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="784a5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="784a5-122">Remarks</span></span>

<span data-ttu-id="784a5-123">Solo se debe llamar a este método cuando es necesario usar un valor distinto de cero para el nad.</span><span class="sxs-lookup"><span data-stu-id="784a5-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="784a5-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="784a5-124">Examples</span></span>

<span data-ttu-id="784a5-125">En el ejemplo siguiente se muestra cómo especificar la dirección de un nodo que se va a usar con la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="784a5-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="784a5-126">En el ejemplo se da por supuesto que byNadValue es una variable de tipo **byte** a la que se asignó previamente un valor y que pISCardCmd es un puntero válido a una instancia de la interfaz **ISCardCmd** .</span><span class="sxs-lookup"><span data-stu-id="784a5-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="784a5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="784a5-127">Requirements</span></span>



| <span data-ttu-id="784a5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="784a5-128">Requirement</span></span> | <span data-ttu-id="784a5-129">Value</span><span class="sxs-lookup"><span data-stu-id="784a5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="784a5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="784a5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="784a5-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="784a5-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="784a5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="784a5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="784a5-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="784a5-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="784a5-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="784a5-134">End of client support</span></span><br/>    | <span data-ttu-id="784a5-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="784a5-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="784a5-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="784a5-136">End of server support</span></span><br/>    | <span data-ttu-id="784a5-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="784a5-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="784a5-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="784a5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="784a5-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="784a5-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="784a5-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="784a5-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="784a5-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="784a5-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="784a5-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="784a5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="784a5-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="784a5-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="784a5-144">IID</span><span class="sxs-lookup"><span data-stu-id="784a5-144">IID</span></span><br/>                      | <span data-ttu-id="784a5-145">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="784a5-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="784a5-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="784a5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="784a5-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="784a5-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
