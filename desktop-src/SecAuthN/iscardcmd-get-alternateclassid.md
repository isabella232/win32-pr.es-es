---
description: Recupera el valor del identificador de clase alternativo.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Método ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649179"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="75eb1-103">ISCardCmd:: get \_ AlternateClassId (método)</span><span class="sxs-lookup"><span data-stu-id="75eb1-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="75eb1-104">\[El método **Get \_ AlternateClassId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="75eb1-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="75eb1-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="75eb1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="75eb1-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="75eb1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="75eb1-107">El método **Get \_ AlternateClassId** recupera el valor del identificador de clase alternativo.</span><span class="sxs-lookup"><span data-stu-id="75eb1-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="75eb1-108">Este método producirá un error a menos que se haya establecido el identificador alternativo mediante una llamada anterior a [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="75eb1-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75eb1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75eb1-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="75eb1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75eb1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75eb1-111">*pbyClass* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75eb1-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75eb1-112">Puntero al byte que contiene el valor de identificador de clase alternativo en la devolución.</span><span class="sxs-lookup"><span data-stu-id="75eb1-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75eb1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75eb1-113">Return value</span></span>

<span data-ttu-id="75eb1-114">El método devuelve los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="75eb1-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="75eb1-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75eb1-115">Return code</span></span>                                                                                    | <span data-ttu-id="75eb1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="75eb1-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75eb1-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="75eb1-118">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="75eb1-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="75eb1-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="75eb1-120">El parámetro *pbyClass* no es válido.</span><span class="sxs-lookup"><span data-stu-id="75eb1-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="75eb1-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="75eb1-122">El identificador de clase alternativo no se ha establecido previamente mediante una llamada a [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="75eb1-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75eb1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75eb1-123">Remarks</span></span>

<span data-ttu-id="75eb1-124">Este método se aplica a las comunicaciones que usan el [*Protocolo T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="75eb1-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="75eb1-125">Para obtener más información, consulte [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="75eb1-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="75eb1-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75eb1-126">Examples</span></span>

<span data-ttu-id="75eb1-127">En el ejemplo siguiente se muestra cómo recuperar el identificador de clase alternativo.</span><span class="sxs-lookup"><span data-stu-id="75eb1-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="75eb1-128">En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="75eb1-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="75eb1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75eb1-129">Requirements</span></span>



| <span data-ttu-id="75eb1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="75eb1-130">Requirement</span></span> | <span data-ttu-id="75eb1-131">Value</span><span class="sxs-lookup"><span data-stu-id="75eb1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75eb1-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75eb1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="75eb1-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="75eb1-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="75eb1-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75eb1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="75eb1-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="75eb1-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75eb1-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="75eb1-136">End of client support</span></span><br/>    | <span data-ttu-id="75eb1-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="75eb1-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="75eb1-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="75eb1-138">End of server support</span></span><br/>    | <span data-ttu-id="75eb1-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75eb1-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="75eb1-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75eb1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="75eb1-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="75eb1-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75eb1-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="75eb1-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75eb1-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75eb1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75eb1-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75eb1-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="75eb1-146">IID</span><span class="sxs-lookup"><span data-stu-id="75eb1-146">IID</span></span><br/>                      | <span data-ttu-id="75eb1-147">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="75eb1-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="75eb1-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="75eb1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75eb1-149">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="75eb1-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="75eb1-150">**Put \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="75eb1-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
