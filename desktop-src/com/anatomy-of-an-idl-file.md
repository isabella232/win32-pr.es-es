---
title: Anatomía de un archivo IDL
description: En estos archivos IDL de ejemplo se muestran las construcciones fundamentales de la definición de interfaz.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "104361801"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="60518-103">Anatomía de un archivo IDL</span><span class="sxs-lookup"><span data-stu-id="60518-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="60518-104">En estos archivos IDL de ejemplo se muestran las construcciones fundamentales de la definición de interfaz.</span><span class="sxs-lookup"><span data-stu-id="60518-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="60518-105">La asignación de memoria, la serialización personalizada y la mensajería asincrónica son solo algunas de las características que se pueden implementar en una interfaz COM personalizada.</span><span class="sxs-lookup"><span data-stu-id="60518-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="60518-106">Los atributos MIDL se utilizan para definir interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="60518-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="60518-107">Para obtener más información sobre la implementación de interfaces y bibliotecas de tipos, incluido un resumen de los atributos MIDL, vea [definiciones de interfaz y bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) en la guía y referencia del programador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="60518-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="60518-108">Para obtener una referencia completa de todos los atributos, palabras clave y directivas de MIDL, vea la [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="60518-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="60518-109">Ejemplo. idl</span><span class="sxs-lookup"><span data-stu-id="60518-109">Example.idl</span></span>

<span data-ttu-id="60518-110">En el siguiente archivo IDL de ejemplo se definen dos interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="60518-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="60518-111">A partir de este archivo IDL, Midl.exe generará código proxy/código auxiliar y archivos de encabezado y serialización.</span><span class="sxs-lookup"><span data-stu-id="60518-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="60518-112">Una sección de línea por línea sigue el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="60518-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="60518-113">La instrucción de [**importación**](/windows/desktop/Midl/import) IDL se usa aquí para traer un archivo de encabezado, Mydefs. h, que contiene los tipos definidos por el usuario, y Unknwn. idl, que contiene la definición de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), de la que se derivan IFace1 y IFace2.</span><span class="sxs-lookup"><span data-stu-id="60518-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="60518-114">El atributo de [**objeto**](/windows/desktop/Midl/object) identifica la interfaz como una interfaz de objeto e indica al compilador de MIDL que genere código de proxy/código auxiliar en lugar del cliente RPC y los códigos auxiliares de servidor.</span><span class="sxs-lookup"><span data-stu-id="60518-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="60518-115">Los métodos de la interfaz de objeto deben tener un tipo de valor devuelto de [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), para permitir que el mecanismo RPC subyacente informe de los errores de las llamadas que no se han podido completar debido a problemas de red.</span><span class="sxs-lookup"><span data-stu-id="60518-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="60518-116">El atributo [**UUID**](/windows/desktop/Midl/uuid) especifica el identificador de interfaz (IID).</span><span class="sxs-lookup"><span data-stu-id="60518-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="60518-117">Cada interfaz, clase y biblioteca de tipos debe identificarse con su propio identificador único.</span><span class="sxs-lookup"><span data-stu-id="60518-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="60518-118">Use el Uuidgen.exe de la utilidad para generar un conjunto de identificadores únicos para las interfaces y otros componentes.</span><span class="sxs-lookup"><span data-stu-id="60518-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="60518-119">La palabra clave [**interface**](/windows/desktop/Midl/interface) define el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="60518-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="60518-120">Todas las interfaces de objeto deben derivar, directa o indirectamente, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="60518-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="60518-121">El parámetro [**en**](/windows/desktop/Midl/in) direccional especifica un parámetro que solo el autor de la llamada establece.</span><span class="sxs-lookup"><span data-stu-id="60518-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="60518-122">El parámetro [**out**](/windows/desktop/Midl/out-idl) especifica los datos que se devuelven al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="60518-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="60518-123">El uso de ambos atributos direccionales en un parámetro especifica que el parámetro se utiliza para enviar datos al método y para devolver datos al llamador.</span><span class="sxs-lookup"><span data-stu-id="60518-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="60518-124">El [**atributo \_ default del puntero**](/windows/desktop/Midl/pointer-default) especifica el tipo de puntero predeterminado ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)o [**ptr**](/windows/desktop/Midl/ptr)) de todos los punteros excepto los incluidos en las listas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="60518-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="60518-125">Si no se especifica ningún tipo predeterminado, MIDL supone que los punteros simples son **únicos**.</span><span class="sxs-lookup"><span data-stu-id="60518-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="60518-126">Sin embargo, si tiene varios niveles de punteros, debe especificar explícitamente un tipo de puntero predeterminado, incluso si desea que el tipo predeterminado sea **único**.</span><span class="sxs-lookup"><span data-stu-id="60518-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="60518-127">En el ejemplo anterior, la matriz BkfstStuff \[ \] es una *matriz compatible*, cuyo tamaño se determina en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="60518-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="60518-128">El atributo [**Max \_ is**](/windows/desktop/Midl/max-is) especifica la variable que contiene el valor máximo para el índice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="60518-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="60518-129">El atributo [**size \_ también se**](/windows/desktop/Midl/size-is) utiliza para especificar el tamaño de una matriz o, como en el ejemplo anterior, varios niveles de punteros.</span><span class="sxs-lookup"><span data-stu-id="60518-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="60518-130">En el ejemplo, se puede realizar la llamada sin conocer de antemano la cantidad de datos que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="60518-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="60518-131">Example2. idl</span><span class="sxs-lookup"><span data-stu-id="60518-131">Example2.idl</span></span>

<span data-ttu-id="60518-132">En el siguiente ejemplo de IDL (que reutiliza las interfaces descritas en el ejemplo IDL anterior) se muestran las distintas formas de generar información de la biblioteca de tipos para las interfaces.</span><span class="sxs-lookup"><span data-stu-id="60518-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="60518-133">El atributo [**HelpString**](/windows/desktop/Midl/helpstring) es opcional; se usa para describir brevemente el objeto o para proporcionar una línea de estado.</span><span class="sxs-lookup"><span data-stu-id="60518-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="60518-134">Estas cadenas de ayuda se pueden leer con un examinador de objetos como el que se proporciona con Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="60518-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="60518-135">El atributo [**dual**](/windows/desktop/Midl/dual) de IFace3 crea una interfaz que es una interfaz de envío y una interfaz com.</span><span class="sxs-lookup"><span data-stu-id="60518-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="60518-136">Dado que se deriva de **IDispatch**, una interfaz dual admite automatización, que es lo que especifica el atributo [**oleautomation**](/windows/desktop/Midl/oleautomation) .</span><span class="sxs-lookup"><span data-stu-id="60518-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="60518-137">IFace3 importa Oaidl. idl para obtener la definición de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="60518-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="60518-138">La instrucción [**Library**](/windows/desktop/Midl/library) define la biblioteca de tipos ExampleLib, que tiene sus propios atributos [**UUID**](/windows/desktop/Midl/uuid), [**HelpString**](/windows/desktop/Midl/helpstring)y [**version**](/windows/desktop/Midl/version) .</span><span class="sxs-lookup"><span data-stu-id="60518-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="60518-139">Dentro de la definición de la biblioteca de tipos, la directiva [**importlib**](/windows/desktop/Midl/importlib) se coloca en una biblioteca de tipos compilada.</span><span class="sxs-lookup"><span data-stu-id="60518-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="60518-140">Todas las definiciones de biblioteca de tipos deben incorporar la biblioteca de tipos base definida en Stdole32. tlb.</span><span class="sxs-lookup"><span data-stu-id="60518-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="60518-141">Esta definición de biblioteca de tipos muestra tres formas diferentes de incluir interfaces en la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="60518-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="60518-142">IFace3 se incluye simplemente haciendo referencia a él en la instrucción Library.</span><span class="sxs-lookup"><span data-stu-id="60518-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="60518-143">La instrucción [**CoClass**](/windows/desktop/Midl/coclass) define una clase de componente completamente nueva, BkfstComponent, que incluye dos interfaces definidas previamente, IFace1 y IFace2.</span><span class="sxs-lookup"><span data-stu-id="60518-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="60518-144">El atributo default designa IFace1 como la interfaz predeterminada.</span><span class="sxs-lookup"><span data-stu-id="60518-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="60518-145">IFace4 se describe en la instrucción Library.</span><span class="sxs-lookup"><span data-stu-id="60518-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="60518-146">El atributo [**PROPPUT**](/windows/desktop/Midl/propput) en el método indica que el método realiza una acción set en una propiedad con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="60518-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="60518-147">El atributo [**propget**](/windows/desktop/Midl/propget) indica que el método recupera información de una propiedad con el mismo nombre que el método.</span><span class="sxs-lookup"><span data-stu-id="60518-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="60518-148">El atributo [**retval**](/windows/desktop/Midl/retval) de methoded designa un parámetro de salida que contiene el valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="60518-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
