---
title: Usar objetos COM en páginas Active Server
description: Puede crear scripts de objetos COM en aplicaciones de Active Server páginas (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356762"
---
# <a name="using-com-objects-in-active-server-pages"></a><span data-ttu-id="dabb2-103">Usar objetos COM en páginas Active Server</span><span class="sxs-lookup"><span data-stu-id="dabb2-103">Using COM Objects in Active Server Pages</span></span>

<span data-ttu-id="dabb2-104">Puede crear scripts de objetos COM en aplicaciones de Active Server páginas (ASP).</span><span class="sxs-lookup"><span data-stu-id="dabb2-104">You can script COM objects in Active Server Pages (ASP) applications.</span></span> <span data-ttu-id="dabb2-105">Para ello, primero debe crear una instancia del objeto utilizando la etiqueta de objeto o llamando al método CreateObject del objeto de servidor ASP.</span><span class="sxs-lookup"><span data-stu-id="dabb2-105">To do so, you must first create an instance of the object either by using the OBJECT tag or by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="dabb2-106">Una vez creado un objeto COM, puede usarlo en scripts posteriores en la página ASP.</span><span class="sxs-lookup"><span data-stu-id="dabb2-106">Once a COM object has been created, you can use it in subsequent scripts on the ASP page.</span></span>

<span data-ttu-id="dabb2-107">Con ASP, puede trabajar con muchos tipos diferentes de motores de scripts, cada uno de los cuales admite un lenguaje de scripting diferente.</span><span class="sxs-lookup"><span data-stu-id="dabb2-107">Using ASP, you can work with many different types of scripting engines, each of which supports a different scripting language.</span></span> <span data-ttu-id="dabb2-108">ASP incluye los motores de scripting de VBScript y JScript.</span><span class="sxs-lookup"><span data-stu-id="dabb2-108">ASP comes with VBScript and JScript scripting engines.</span></span> <span data-ttu-id="dabb2-109">También puede conectar motores de scripting desarrollados por otras compañías para admitir lenguajes como PerlScript, PScript, Python y otros.</span><span class="sxs-lookup"><span data-stu-id="dabb2-109">You can also plug in scripting engines developed by other companies to support languages such as PerlScript, PScript, Python, and others.</span></span>

<span data-ttu-id="dabb2-110">Si no establece el lenguaje de scripting para una página ASP, VBScript es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dabb2-110">If you do not set the scripting language for an ASP page, VBScript is the default.</span></span> <span data-ttu-id="dabb2-111">Para especificar un lenguaje de scripting distinto de VBScript, incluya una línea como la siguiente en la parte superior de cada página ASP:</span><span class="sxs-lookup"><span data-stu-id="dabb2-111">To specify a scripting language other than VBScript, include a line such as the following at the top of each ASP page:</span></span>

``` syntax
<%@ LANGUAGE=JScript %>
 
```

<span data-ttu-id="dabb2-112">Para usar un objeto COM en una página ASP, primero debe crear una instancia de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="dabb2-112">To use a COM object in an ASP page, you must first create an instance of that object.</span></span> <span data-ttu-id="dabb2-113">Para ello, use la etiqueta OBJECT y especifique el valor "SERVER" para el atributo runas, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="dabb2-113">You do this by using the OBJECT tag and specifying the value "SERVER" for the RUNAT attribute, as shown in the following example.</span></span> <span data-ttu-id="dabb2-114">De forma predeterminada, la etiqueta de objeto crea una instancia del objeto en el cliente.</span><span class="sxs-lookup"><span data-stu-id="dabb2-114">By default, the OBJECT tag creates an instance of the object on the client.</span></span> <span data-ttu-id="dabb2-115">Al establecer el atributo RUNAt en SERVER, se crea el objeto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="dabb2-115">Setting the RUNAT attribute to SERVER causes the object to be created on the server.</span></span> <span data-ttu-id="dabb2-116">El objeto se debe ejecutar en el servidor para que lo use ASP.</span><span class="sxs-lookup"><span data-stu-id="dabb2-116">The object must run on the server in order to be used by ASP.</span></span>

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

<span data-ttu-id="dabb2-117">También puede crear una instancia de un objeto COM en una página ASP llamando al método CreateObject del objeto de servidor ASP.</span><span class="sxs-lookup"><span data-stu-id="dabb2-117">You can also create an instance of a COM object on an ASP page by calling the CreateObject method of the ASP Server object.</span></span> <span data-ttu-id="dabb2-118">El uso de Server. CreateObject es más lento que la creación del objeto mediante una etiqueta de objeto, pero es ligeramente más legible porque especifica el identificador de programación en lugar del identificador de clase del objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dabb2-118">Using Server.CreateObject is slower than creating the object using an OBJECT tag, but it is slightly more readable because it specifies the programmatic identifier instead of the class identifier of the COM object.</span></span> <span data-ttu-id="dabb2-119">El objeto de servidor se expone mediante ASP y no es necesario crearlo.</span><span class="sxs-lookup"><span data-stu-id="dabb2-119">The Server object is exposed by ASP and does not need to be created.</span></span> <span data-ttu-id="dabb2-120">Cómo llamar a Server. CreateObject se ilustra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="dabb2-120">How to call Server.CreateObject is illustrated in the following examples.</span></span> <span data-ttu-id="dabb2-121">El primer ejemplo es VBScript:</span><span class="sxs-lookup"><span data-stu-id="dabb2-121">The first example is VBScript:</span></span>

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="dabb2-122">El ejemplo siguiente es JScript:</span><span class="sxs-lookup"><span data-stu-id="dabb2-122">The next example is JScript:</span></span>

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

<span data-ttu-id="dabb2-123">Llamar a CreateObject es más lento que usar la etiqueta de objeto para crear un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dabb2-123">Calling CreateObject is slower than using the OBJECT tag to create a COM object.</span></span> <span data-ttu-id="dabb2-124">En aplicaciones en las que el rendimiento es crítico, debe usar la etiqueta de objeto.</span><span class="sxs-lookup"><span data-stu-id="dabb2-124">In applications where performance is critical, you should use the OBJECT tag.</span></span>

<span data-ttu-id="dabb2-125">Después de crear una instancia del objeto COM, puede usarla en scripts.</span><span class="sxs-lookup"><span data-stu-id="dabb2-125">After you have created an instance of the COM object, you can use it in scripts.</span></span> <span data-ttu-id="dabb2-126">Esto se ilustra en el ejemplo de VBScript siguiente, que establece el valor de la propiedad border del objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dabb2-126">Doing this is illustrated in the VBScript example following, which sets the value of the COM object's Border property.</span></span>

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a><span data-ttu-id="dabb2-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dabb2-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dabb2-128">Scripting con objetos COM</span><span class="sxs-lookup"><span data-stu-id="dabb2-128">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




