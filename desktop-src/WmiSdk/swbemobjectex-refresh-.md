---
description: Actualiza los datos de los objetos que tienen datos proporcionados por un proveedor de rendimiento, como las clases de contador de rendimiento. Puede obtener datos actualizados más rápidamente y sin una llamada a SWbemServices. Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Método SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715734"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="bee52-104">SWbemObjectEx. Refresh ( \_ método)</span><span class="sxs-lookup"><span data-stu-id="bee52-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="bee52-105">El **método \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) actualiza los datos de los objetos que tienen datos proporcionados por un proveedor de rendimiento, como las [clases de contador de rendimiento](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="bee52-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="bee52-106">Puede obtener datos actualizados más rápidamente y sin una llamada a [**SWbemServices. Get \_**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="bee52-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="bee52-107">Para obtener más información sobre esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bee52-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bee52-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bee52-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bee52-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bee52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bee52-110">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bee52-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bee52-111">Marcas de operación reservadas que, si se especifican, deben ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="bee52-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="bee52-112">*objWbemNamedValueSet* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bee52-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bee52-113">Objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que establece el contexto de la operación.</span><span class="sxs-lookup"><span data-stu-id="bee52-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bee52-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bee52-114">Return value</span></span>

<span data-ttu-id="bee52-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bee52-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bee52-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bee52-116">Error codes</span></span>

<span data-ttu-id="bee52-117">Después de completar el **método \_ Refresh** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="bee52-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bee52-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bee52-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bee52-119">Se produjo un error interno en el proveedor, aunque la operación era válida.</span><span class="sxs-lookup"><span data-stu-id="bee52-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="bee52-120">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="bee52-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bee52-121">No se encontró el formato solicitado.</span><span class="sxs-lookup"><span data-stu-id="bee52-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="bee52-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="bee52-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bee52-123">Uno de los parámetros de la llamada no es correcto.</span><span class="sxs-lookup"><span data-stu-id="bee52-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="bee52-124">**wbemErrRefresherBusy** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="bee52-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="bee52-125">El actualizador está ocupado con otra operación.</span><span class="sxs-lookup"><span data-stu-id="bee52-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="bee52-126">**wbemPartialResults** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="bee52-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="bee52-127">No todos los objetos, enumeradores o actualizaciones anidadas se actualizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="bee52-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="bee52-128">Este valor devuelto no es un error, pero indica que la operación estaba incompleta.</span><span class="sxs-lookup"><span data-stu-id="bee52-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bee52-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bee52-129">Examples</span></span>

<span data-ttu-id="bee52-130">En el ejemplo de código de script siguiente se muestra cómo obtener contadores de rendimiento sin procesar y cocidos para el proceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="bee52-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="bee52-131">Los objetos se actualizan cada dos segundos y se muestran las propiedades.</span><span class="sxs-lookup"><span data-stu-id="bee52-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="bee52-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bee52-132">Requirements</span></span>



| <span data-ttu-id="bee52-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bee52-133">Requirement</span></span> | <span data-ttu-id="bee52-134">Value</span><span class="sxs-lookup"><span data-stu-id="bee52-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bee52-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee52-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bee52-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bee52-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bee52-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee52-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bee52-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bee52-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bee52-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bee52-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bee52-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bee52-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bee52-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bee52-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="bee52-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bee52-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bee52-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bee52-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee52-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bee52-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bee52-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="bee52-145">CLSID</span></span><br/>                    | <span data-ttu-id="bee52-146">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="bee52-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="bee52-147">IID</span><span class="sxs-lookup"><span data-stu-id="bee52-147">IID</span></span><br/>                      | <span data-ttu-id="bee52-148">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="bee52-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bee52-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="bee52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee52-150">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="bee52-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="bee52-151">Supervisión de datos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="bee52-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

