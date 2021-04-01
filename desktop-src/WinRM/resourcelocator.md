---
title: Objeto ResourceLocator (WSManDisp. h)
description: Proporciona la ruta de acceso a un recurso. Puede usar un objeto ResourceLocator en lugar de un URI de recurso en operaciones de objetos de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Objeto ResourceLocator Administración remota de Windows
- Administración remota de Windows de objeto ResourceLocator, descrito
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149992"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="f64a7-106">Objeto ResourceLocator</span><span class="sxs-lookup"><span data-stu-id="f64a7-106">ResourceLocator object</span></span>

<span data-ttu-id="f64a7-107">Objeto que proporciona la ruta de acceso a un recurso.</span><span class="sxs-lookup"><span data-stu-id="f64a7-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="f64a7-108">Puede usar un objeto **ResourceLocator** en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="f64a7-109">Este objeto le permite:</span><span class="sxs-lookup"><span data-stu-id="f64a7-109">This object enables you to:</span></span>

-   <span data-ttu-id="f64a7-110">Agregue uno o más [*selectores*](windows-remote-management-glossary.md) que identifiquen una instancia concreta de un recurso.</span><span class="sxs-lookup"><span data-stu-id="f64a7-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="f64a7-111">Esto es lo mismo que proporcionar un valor de clave en el URI de recurso para un recurso que utiliza claves.</span><span class="sxs-lookup"><span data-stu-id="f64a7-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="f64a7-112">Para obtener más información, vea [**ResourceLocator. AddSelector**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="f64a7-113">Puede realizar una operación similar mediante el parámetro de *filtro* en una llamada a [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="f64a7-114">Especifique una ruta de acceso de [*fragmento*](windows-remote-management-glossary.md) y un dialecto para obtener solo una propiedad de un recurso.</span><span class="sxs-lookup"><span data-stu-id="f64a7-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="f64a7-115">También puede especificar uno o todos los elementos de una propiedad de matriz proporcionando el índice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f64a7-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="f64a7-116">Para obtener más información, vea [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="f64a7-117">Agregue una o varias [*Opciones*](windows-remote-management-glossary.md) que un origen de datos pueda necesitar para procesar una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f64a7-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="f64a7-118">Para obtener más información, consulte [**ResourceLocator. AddOption**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="f64a7-119">Para obtener más información, consulte [consultas para instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="f64a7-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="f64a7-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="f64a7-120">Members</span></span>

<span data-ttu-id="f64a7-121">El objeto **ResourceLocator** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f64a7-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="f64a7-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="f64a7-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="f64a7-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f64a7-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f64a7-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="f64a7-124">Methods</span></span>

<span data-ttu-id="f64a7-125">El objeto **ResourceLocator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f64a7-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="f64a7-126">Método</span><span class="sxs-lookup"><span data-stu-id="f64a7-126">Method</span></span>                                                   | <span data-ttu-id="f64a7-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f64a7-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64a7-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="f64a7-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="f64a7-129">Agrega datos adicionales necesarios para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f64a7-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="f64a7-130">**AddSelector**</span><span class="sxs-lookup"><span data-stu-id="f64a7-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="f64a7-131">Agrega un [*selector*](windows-remote-management-glossary.md) al objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="f64a7-132">**ClearOptions**</span><span class="sxs-lookup"><span data-stu-id="f64a7-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="f64a7-133">Quita todas [*las opciones*](windows-remote-management-glossary.md) del objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="f64a7-134">**ClearSelectors**</span><span class="sxs-lookup"><span data-stu-id="f64a7-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="f64a7-135">Quita todos los selectores de un objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="f64a7-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f64a7-136">Properties</span></span>

<span data-ttu-id="f64a7-137">El objeto **ResourceLocator** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f64a7-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="f64a7-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f64a7-138">Property</span></span>                                                                          | <span data-ttu-id="f64a7-139">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f64a7-139">Access type</span></span>           | <span data-ttu-id="f64a7-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="f64a7-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64a7-141">**FragmentDialect**</span><span class="sxs-lookup"><span data-stu-id="f64a7-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="f64a7-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f64a7-142">Read/write</span></span><br/> | <span data-ttu-id="f64a7-143">Obtiene o establece el dialecto del lenguaje para un [*fragmento*](windows-remote-management-glossary.md)de [*recursos*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="f64a7-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="f64a7-144">**FragmentPath**</span><span class="sxs-lookup"><span data-stu-id="f64a7-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="f64a7-145">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f64a7-145">Read/write</span></span><br/> | <span data-ttu-id="f64a7-146">Obtiene o establece la ruta de acceso de un [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) o propiedad.</span><span class="sxs-lookup"><span data-stu-id="f64a7-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="f64a7-147">**MustUnderstandOptions**</span><span class="sxs-lookup"><span data-stu-id="f64a7-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="f64a7-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f64a7-148">Read/write</span></span><br/> | <span data-ttu-id="f64a7-149">Obtiene o establece el valor de **MustUnderstandOptions** para el objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="f64a7-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="f64a7-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="f64a7-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f64a7-151">Read/write</span></span><br/> | <span data-ttu-id="f64a7-152">Obtiene o establece el [*URI de recurso*](windows-remote-management-glossary.md) en un objeto **ResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f64a7-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f64a7-153">Remarks</span></span>

<span data-ttu-id="f64a7-154">El objeto **ResourceLocator** corresponde a la interfaz **IWSManResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="f64a7-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="f64a7-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f64a7-155">Examples</span></span>

<span data-ttu-id="f64a7-156">En el siguiente ejemplo de código de VBScript se obtienen las propiedades **NumberOfLogicalProcessors** y **NumberOfCores** de una instancia específica del [**\_ procesador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="f64a7-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f64a7-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f64a7-157">Requirements</span></span>



| <span data-ttu-id="f64a7-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="f64a7-158">Requirement</span></span> | <span data-ttu-id="f64a7-159">Value</span><span class="sxs-lookup"><span data-stu-id="f64a7-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64a7-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f64a7-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f64a7-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f64a7-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f64a7-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f64a7-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f64a7-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f64a7-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f64a7-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f64a7-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="f64a7-165"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f64a7-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f64a7-166">IDL</span><span class="sxs-lookup"><span data-stu-id="f64a7-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f64a7-167"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f64a7-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f64a7-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f64a7-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="f64a7-169"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f64a7-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f64a7-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f64a7-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f64a7-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f64a7-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f64a7-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="f64a7-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64a7-173">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="f64a7-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

