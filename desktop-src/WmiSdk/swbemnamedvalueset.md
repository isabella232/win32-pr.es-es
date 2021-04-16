---
description: Un objeto SWbemNamedValueSet es una colección de objetos SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objeto SWbemNamedValueSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706055"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="6f675-103">Objeto SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6f675-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="6f675-104">Un objeto **SWbemNamedValueSet** es una colección de objetos [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6f675-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="6f675-105">Los métodos y las propiedades de **SWbemNamedValueSet** se usan principalmente para enviar más información a los proveedores al enviar ciertas llamadas a WMI.</span><span class="sxs-lookup"><span data-stu-id="6f675-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="6f675-106">Todas las llamadas en [**SWbemServices**](swbemservices.md)y algunas llamadas en [**SWbemObject**](swbemobject.md)toman un parámetro opcional que es un objeto de este tipo.</span><span class="sxs-lookup"><span data-stu-id="6f675-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="6f675-107">Un cliente puede agregar información a un objeto **SWbemNamedValueSet** y enviar el objeto **SWbemNamedValueSet** con la llamada como uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f675-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="6f675-108">Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="6f675-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="6f675-109">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6f675-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="6f675-110">Importante: si es posible, no utilice este mecanismo porque puede interrumpir el modelo de acceso uniforme que constituye la base de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f675-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="6f675-111">Si un proveedor utiliza este mecanismo, es importante que este mecanismo se use de la manera más moderada posible.</span><span class="sxs-lookup"><span data-stu-id="6f675-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="6f675-112">Si un proveedor requiere una gran cantidad de información de contexto muy específica para responder a una solicitud, todos los clientes deben codificarse para proporcionar esta información.</span><span class="sxs-lookup"><span data-stu-id="6f675-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="6f675-113">Este mecanismo le permite tener acceso a estos proveedores, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="6f675-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="6f675-114">Un objeto **SWbemNamedValueSet** es una colección de elementos [**SWbemNamedValue**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6f675-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="6f675-115">Estos elementos se agregan a la colección mediante el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="6f675-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="6f675-116">Se quitan mediante el método [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) y se recuperan mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="6f675-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="6f675-117">Puede tener acceso a los métodos para rellenar cualquier información de contexto requerida por un proveedor dinámico.</span><span class="sxs-lookup"><span data-stu-id="6f675-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="6f675-118">Después de llamar a uno de los métodos [**SWbemServices**](swbemservices.md) , puede volver a usar el objeto **SWbemNamedValueSet** para otra llamada.</span><span class="sxs-lookup"><span data-stu-id="6f675-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="6f675-119">El proveedor subyacente determina la información contenida en un objeto **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="6f675-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="6f675-120">WMI no hace uso de la información, sino que simplemente la reenvía al proveedor.</span><span class="sxs-lookup"><span data-stu-id="6f675-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="6f675-121">Los proveedores deben publicar la información de contexto que requieren para atender las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="6f675-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="6f675-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f675-122">Members</span></span>

<span data-ttu-id="6f675-123">El objeto **SWbemNamedValueSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f675-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="6f675-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f675-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f675-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f675-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f675-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f675-126">Methods</span></span>

<span data-ttu-id="6f675-127">El objeto **SWbemNamedValueSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6f675-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="6f675-128">Método</span><span class="sxs-lookup"><span data-stu-id="6f675-128">Method</span></span>                                            | <span data-ttu-id="6f675-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f675-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f675-130">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="6f675-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="6f675-131">Agrega un objeto [**SWbemNamedValue**](swbemnamedvalue.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="6f675-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="6f675-132">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="6f675-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="6f675-133">Realiza una copia de esta colección **SWbemNamedValueSet** .</span><span class="sxs-lookup"><span data-stu-id="6f675-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="6f675-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="6f675-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="6f675-135">Quita todos los elementos de la colección, con lo que el objeto **SWbemNamedValueSet** está vacío.</span><span class="sxs-lookup"><span data-stu-id="6f675-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="6f675-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f675-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="6f675-137">Recupera un objeto [**SWbemNamedValue**](swbemnamedvalue.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="6f675-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="6f675-138">Este es el método predeterminado del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f675-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="6f675-139">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="6f675-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="6f675-140">Quita un objeto [**SWbemNamedValue**](swbemnamedvalue.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="6f675-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="6f675-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f675-141">Properties</span></span>

<span data-ttu-id="6f675-142">El objeto **SWbemNamedValueSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6f675-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="6f675-143">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f675-143">Property</span></span>                                             | <span data-ttu-id="6f675-144">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6f675-144">Access type</span></span>          | <span data-ttu-id="6f675-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f675-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="6f675-146">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="6f675-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="6f675-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f675-147">Read-only</span></span><br/> | <span data-ttu-id="6f675-148">Número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="6f675-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6f675-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6f675-149">Examples</span></span>

<span data-ttu-id="6f675-150">El siguiente ejemplo de VBScript muestra la manipulación de los conjuntos de valores con nombre, en el caso de que el valor con nombre sea un tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="6f675-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="6f675-151">El siguiente ejemplo de Perl muestra la manipulación de los conjuntos de valores con nombre, en el caso de que el valor con nombre sea un tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="6f675-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="6f675-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f675-152">Requirements</span></span>



| <span data-ttu-id="6f675-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f675-153">Requirement</span></span> | <span data-ttu-id="6f675-154">Value</span><span class="sxs-lookup"><span data-stu-id="6f675-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f675-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f675-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6f675-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f675-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f675-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f675-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6f675-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f675-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f675-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f675-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f675-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f675-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f675-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f675-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f675-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f675-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f675-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f675-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f675-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f675-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f675-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f675-165">CLSID</span></span><br/>                    | <span data-ttu-id="6f675-166">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6f675-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="6f675-167">IID</span><span class="sxs-lookup"><span data-stu-id="6f675-167">IID</span></span><br/>                      | <span data-ttu-id="6f675-168">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="6f675-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="6f675-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f675-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f675-170">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="6f675-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




