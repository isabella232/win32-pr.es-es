---
description: Devuelve el campo le de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Método ISCardCmd:: get_LeField (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818507"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="74a40-103">ISCardCmd:: get \_ LeField (método)</span><span class="sxs-lookup"><span data-stu-id="74a40-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="74a40-104">\[El método **Get \_ LeField** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="74a40-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74a40-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="74a40-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="74a40-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="74a40-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="74a40-107">El método **Get \_ LeField** devuelve el campo le de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="74a40-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="74a40-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74a40-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="74a40-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74a40-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a40-110">*plSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74a40-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74a40-111">Puntero al valor del campo le en la devolución.</span><span class="sxs-lookup"><span data-stu-id="74a40-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a40-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74a40-112">Return value</span></span>

<span data-ttu-id="74a40-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="74a40-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="74a40-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="74a40-114">Return code</span></span>                                                                                  | <span data-ttu-id="74a40-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="74a40-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="74a40-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="74a40-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="74a40-117">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="74a40-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="74a40-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="74a40-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="74a40-119">El parámetro *plSize* no es válido.</span><span class="sxs-lookup"><span data-stu-id="74a40-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="74a40-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="74a40-120">Examples</span></span>

<span data-ttu-id="74a40-121">En el ejemplo siguiente se muestra cómo recuperar el valor del campo le de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="74a40-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="74a40-122">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="74a40-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="74a40-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74a40-123">Requirements</span></span>



| <span data-ttu-id="74a40-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a40-124">Requirement</span></span> | <span data-ttu-id="74a40-125">Value</span><span class="sxs-lookup"><span data-stu-id="74a40-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74a40-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74a40-126">Minimum supported client</span></span><br/> | <span data-ttu-id="74a40-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="74a40-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74a40-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74a40-128">Minimum supported server</span></span><br/> | <span data-ttu-id="74a40-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74a40-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74a40-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="74a40-130">End of client support</span></span><br/>    | <span data-ttu-id="74a40-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74a40-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="74a40-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="74a40-132">End of server support</span></span><br/>    | <span data-ttu-id="74a40-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74a40-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="74a40-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74a40-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="74a40-135"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="74a40-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="74a40-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="74a40-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="74a40-137"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74a40-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74a40-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74a40-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74a40-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74a40-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74a40-140">IID</span><span class="sxs-lookup"><span data-stu-id="74a40-140">IID</span></span><br/>                      | <span data-ttu-id="74a40-141">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="74a40-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="74a40-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="74a40-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a40-143">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="74a40-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
