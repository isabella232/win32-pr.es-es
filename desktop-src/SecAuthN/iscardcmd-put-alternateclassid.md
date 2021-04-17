---
description: Especifica un nuevo identificador de clase alternativo en la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd: método de ut_AlternateClassId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652426"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="a3a9f-103">ISCardCmd::p \_ método AlternateClassId UT</span><span class="sxs-lookup"><span data-stu-id="a3a9f-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="a3a9f-104">\[El método **Put \_ AlternateClassId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3a9f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3a9f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a3a9f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a3a9f-107">El método **Put \_ AlternateClassId** especifica un nuevo identificador de clase alternativo en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a3a9f-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a9f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3a9f-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="a3a9f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3a9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a9f-110">*byClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3a9f-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3a9f-111">Identificador de clase alternativo.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-111">Alternate class identifier.</span></span> <span data-ttu-id="a3a9f-112">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a9f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a9f-113">Return value</span></span>

<span data-ttu-id="a3a9f-114">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a3a9f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a9f-115">Return code</span></span>                                                                                  | <span data-ttu-id="a3a9f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3a9f-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a3a9f-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a9f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a3a9f-118">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a3a9f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a3a9f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a3a9f-120">El parámetro *byClass* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3a9f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3a9f-121">Remarks</span></span>

<span data-ttu-id="a3a9f-122">Con las comunicaciones que usan el [*Protocolo T = 0*](../secgloss/t-gly.md), las APDU pueden generar automáticamente comandos de tarjeta adicionales y enviarlos a la unidad de datos de protocolo de transmisión (TPDU).</span><span class="sxs-lookup"><span data-stu-id="a3a9f-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="a3a9f-123">Los comandos adicionales suelen usar el mismo identificador de clase que el comando original. especificar un nuevo identificador de clase por medio de este método permite que los comandos generados automáticamente utilicen el nuevo identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="a3a9f-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="a3a9f-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3a9f-124">Examples</span></span>

<span data-ttu-id="a3a9f-125">En el ejemplo siguiente se muestra cómo establecer un nuevo identificador de clase alternativo en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a3a9f-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a3a9f-126">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a9f-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a3a9f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a9f-127">Requirements</span></span>



| <span data-ttu-id="a3a9f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a9f-128">Requirement</span></span> | <span data-ttu-id="a3a9f-129">Value</span><span class="sxs-lookup"><span data-stu-id="a3a9f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a9f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a9f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a9f-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a9f-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a3a9f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3a9f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a9f-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3a9f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3a9f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a3a9f-134">End of client support</span></span><br/>    | <span data-ttu-id="a3a9f-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3a9f-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a3a9f-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a3a9f-136">End of server support</span></span><br/>    | <span data-ttu-id="a3a9f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3a9f-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a3a9f-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3a9f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3a9f-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3a9f-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3a9f-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a3a9f-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3a9f-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3a9f-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3a9f-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3a9f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a9f-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a9f-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3a9f-144">IID</span><span class="sxs-lookup"><span data-stu-id="a3a9f-144">IID</span></span><br/>                      | <span data-ttu-id="a3a9f-145">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a3a9f-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a3a9f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3a9f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a9f-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a3a9f-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a3a9f-148">**obtener \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="a3a9f-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
