---
description: Devuelve el SWbemObject asociado al índice especificado en la colección.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Método SWbemObjectSet. ItemIndex (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706979"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="f111e-103">SWbemObjectSet. ItemIndex (método)</span><span class="sxs-lookup"><span data-stu-id="f111e-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="f111e-104">El método **itemIndex** devuelve el [**SWbemObject**](swbemobject.md) asociado con el índice especificado en la colección.</span><span class="sxs-lookup"><span data-stu-id="f111e-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="f111e-105">El índice indica la posición del elemento dentro de la colección.</span><span class="sxs-lookup"><span data-stu-id="f111e-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="f111e-106">La numeración de la colección comienza en cero.</span><span class="sxs-lookup"><span data-stu-id="f111e-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="f111e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f111e-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="f111e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f111e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f111e-109">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="f111e-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="f111e-110">Índice del elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="f111e-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f111e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f111e-111">Return value</span></span>

<span data-ttu-id="f111e-112">Si se realiza correctamente, el objeto [**SWbemObject**](swbemobject.md) solicitado devuelve.</span><span class="sxs-lookup"><span data-stu-id="f111e-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f111e-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f111e-113">Error codes</span></span>

<span data-ttu-id="f111e-114">Una vez finalizado el método [**Item**](swbemobjectset-item.md) , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="f111e-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="f111e-115">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f111e-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f111e-116">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="f111e-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f111e-117">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f111e-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f111e-118">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="f111e-118">Invalid parameter was specified.</span></span> <span data-ttu-id="f111e-119">Se devuelve este error si se proporciona un número de índice negativo.</span><span class="sxs-lookup"><span data-stu-id="f111e-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="f111e-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f111e-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f111e-121">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="f111e-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f111e-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f111e-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f111e-123">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="f111e-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f111e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f111e-124">Remarks</span></span>

<span data-ttu-id="f111e-125">El método **itemIndex** permite que los scripts y las aplicaciones de los clientes WMI escritos en cualquier lenguaje sean una manera uniforme de manipular una colección como una matriz.</span><span class="sxs-lookup"><span data-stu-id="f111e-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="f111e-126">Este método se puede usar con colecciones [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="f111e-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="f111e-127">Las consultas, como [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. References**](swbemservices-referencesto.md), [**SWbemServices. instances**](swbemservices-instancesof.md)o [**SWbemServices.ExecQuery**](swbemservices-execquery.md) devuelven colecciones de **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="f111e-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="f111e-128">El método **itemIndex** no funciona con colecciones que no contienen [**SWbemObjects**](swbemobject.md), como [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)y [**SWbemQualifierSet**](swbemqualifierset.md).</span><span class="sxs-lookup"><span data-stu-id="f111e-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="f111e-129">**ItemIndex** también se puede utilizar para obtener la instancia única de una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="f111e-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="f111e-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f111e-130">Examples</span></span>

<span data-ttu-id="f111e-131">En el siguiente ejemplo de código de VBScript se consulta una colección de todas las instancias de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) y, a continuación, se muestran los nombres de los tres primeros procesos.</span><span class="sxs-lookup"><span data-stu-id="f111e-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="f111e-132">Solo existe una instancia de [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) para cada instalación de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f111e-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="f111e-133">La creación de la ruta de acceso [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para obtener la instancia única es difícil, por lo que los scripts suelen enumerar **Win32 \_ OperatingSystem** aunque solo haya una instancia disponible.</span><span class="sxs-lookup"><span data-stu-id="f111e-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="f111e-134">En el ejemplo de código de VBScript siguiente se muestra cómo utilizar el método **itemIndex** para llegar a un sistema **\_ operativo de Win32** sin usar un bucle **for each** .</span><span class="sxs-lookup"><span data-stu-id="f111e-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="f111e-135">El siguiente ejemplo de código de VBScript obtiene instancias asociadas con el [**\_ OperatingSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), como [**\_ SystemOperatingSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span><span class="sxs-lookup"><span data-stu-id="f111e-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="f111e-136">La siguiente salida de ejemplo de código muestra las instancias asociadas a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="f111e-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="f111e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f111e-137">Requirements</span></span>



| <span data-ttu-id="f111e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f111e-138">Requirement</span></span> | <span data-ttu-id="f111e-139">Value</span><span class="sxs-lookup"><span data-stu-id="f111e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f111e-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f111e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f111e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f111e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f111e-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f111e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f111e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f111e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f111e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f111e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f111e-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f111e-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f111e-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f111e-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f111e-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f111e-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f111e-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f111e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f111e-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f111e-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f111e-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="f111e-150">CLSID</span></span><br/>                    | <span data-ttu-id="f111e-151">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="f111e-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="f111e-152">IID</span><span class="sxs-lookup"><span data-stu-id="f111e-152">IID</span></span><br/>                      | <span data-ttu-id="f111e-153">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="f111e-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="f111e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f111e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f111e-155">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="f111e-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

