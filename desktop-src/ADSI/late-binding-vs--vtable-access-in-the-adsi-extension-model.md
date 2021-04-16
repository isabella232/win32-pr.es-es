---
title: Enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI
description: Una interfaz dual permite el acceso de vtable directo a todas sus funciones mientras no una interfaz de envío.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI ADSI
- extensiones ADSI, enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI
- ADSI ADSI, Visual Basic de código de ejemplo, uso de IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656414"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="8229d-106">Enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI</span><span class="sxs-lookup"><span data-stu-id="8229d-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="8229d-107">Una interfaz dual permite el acceso de vtable directo a todas sus funciones mientras no una interfaz de envío.</span><span class="sxs-lookup"><span data-stu-id="8229d-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="8229d-108">Un cliente de C/C++ puede consultar un puntero de interfaz dual y usar el acceso de vtable directo para invocar sus funciones.</span><span class="sxs-lookup"><span data-stu-id="8229d-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="8229d-109">Esto proporciona un acceso más rápido que la invocación de la función mediante las funciones [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="8229d-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="8229d-110">Esto es especialmente cierto en el modelo de extensión, ya que todas las interfaces duales de un objeto de extensión deben delegar sus funciones **GetIDsOfNames** e **Invoke** primero al agregador (ADSI).</span><span class="sxs-lookup"><span data-stu-id="8229d-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="8229d-111">Después, el agregador debe realizar pasos internos adicionales para identificar qué objeto de extensión, posiblemente incluido el propio agregador, proporciona compatibilidad para la función llamada y redirige la llamada al objeto adecuado.</span><span class="sxs-lookup"><span data-stu-id="8229d-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="8229d-112">Visual Basic también invoca una función de interfaz dual mediante el acceso directo a una tabla vtable, si tiene un puntero a la interfaz y acceso a los datos de tipo de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="8229d-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="8229d-113">Los clientes ADSI escritos en Visual Basic pueden especificar un puntero a una interfaz dual, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explícitamente, y, por tanto, habilitar el acceso de vtable a las funciones de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="8229d-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="8229d-114">Dado que una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) no admite el acceso a vtable, no se aplica este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8229d-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="8229d-115">Es decir, siempre se invoca una función de envío a través de las funciones [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) únicamente.</span><span class="sxs-lookup"><span data-stu-id="8229d-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="8229d-116">Las versiones actuales de VBScript y JScript tampoco admiten el acceso vtable.</span><span class="sxs-lookup"><span data-stu-id="8229d-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="8229d-117">Por lo tanto, una interfaz dual en un entorno de VBScript o JScript funciona como una interfaz de envío.</span><span class="sxs-lookup"><span data-stu-id="8229d-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 