---
title: Incrustar objetos COM en páginas web
description: Puede usar objetos COM en páginas Web. Para ello, primero cree una instancia de ese objeto COM. Después de crear una instancia de objeto, puede usarla en scripts posteriores de esa página web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356947"
---
# <a name="embedding-com-objects-in-web-pages"></a><span data-ttu-id="c75ab-105">Incrustar objetos COM en páginas web</span><span class="sxs-lookup"><span data-stu-id="c75ab-105">Embedding COM Objects in Web Pages</span></span>

<span data-ttu-id="c75ab-106">Puede usar objetos COM en páginas Web.</span><span class="sxs-lookup"><span data-stu-id="c75ab-106">You can use COM objects in webpages.</span></span> <span data-ttu-id="c75ab-107">Para ello, primero cree una instancia de ese objeto COM.</span><span class="sxs-lookup"><span data-stu-id="c75ab-107">To do this, first create an instance of that COM object.</span></span> <span data-ttu-id="c75ab-108">Después de crear una instancia de objeto, puede usarla en scripts posteriores de esa página web.</span><span class="sxs-lookup"><span data-stu-id="c75ab-108">After an object instance is created, you can use it in subsequent scripts on that webpage.</span></span>

<span data-ttu-id="c75ab-109">Para crear una instancia de objeto COM en una página web, puede usar una etiqueta de objeto.</span><span class="sxs-lookup"><span data-stu-id="c75ab-109">To create a COM object instance in a webpage, you can use an OBJECT tag.</span></span> <span data-ttu-id="c75ab-110">Como alternativa, si el lenguaje de scripting proporciona una forma nativa de crear objetos COM, puede crear una instancia de objeto mediante un script.</span><span class="sxs-lookup"><span data-stu-id="c75ab-110">Alternatively, if your scripting language provides a native way to create COM objects, you can create an object instance using script.</span></span>

<span data-ttu-id="c75ab-111">Tenga en cuenta que la incrustación de objetos COM en páginas web solo funciona con los exploradores que admiten ActiveX y COM, por ejemplo, Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c75ab-111">Note that embedding COM objects in webpages only works with browsers that support ActiveX and COM, for example Internet Explorer.</span></span>

<span data-ttu-id="c75ab-112">En el ejemplo siguiente se muestra cómo usar la etiqueta de objeto para insertar un objeto COM en una página web:</span><span class="sxs-lookup"><span data-stu-id="c75ab-112">The following example illustrates using the OBJECT tag to embed a COM object in a webpage:</span></span>

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

<span data-ttu-id="c75ab-113">También puede crear una instancia de objeto COM en un script, si el lenguaje de scripting proporciona una manera de crear objetos COM.</span><span class="sxs-lookup"><span data-stu-id="c75ab-113">You can also create a COM object instance in script, if your scripting language provides a way to create COM objects.</span></span> <span data-ttu-id="c75ab-114">Por ejemplo, VBScript proporciona el método CreateObject y JScript proporciona el objeto ActiveXObject.</span><span class="sxs-lookup"><span data-stu-id="c75ab-114">For example, VBScript provides the CreateObject method and JScript provides the ActiveXObject object.</span></span> <span data-ttu-id="c75ab-115">La creación de objetos en el script se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c75ab-115">Creating objects in script is illustrated in the following examples.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

<span data-ttu-id="c75ab-116">Además del método CreateObject y el objeto ActiveXObject, tanto VBScript como JScript proporcionan el método GetObject, que devuelve una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="c75ab-116">In addition to the CreateObject method and the ActiveXObject object, both VBScript and JScript provide the method GetObject, which returns an object instance.</span></span>

<span data-ttu-id="c75ab-117">Una vez creado un objeto COM, puede hacer referencia a él en scripts posteriores mediante el identificador especificado en el atributo ID de la etiqueta de objeto.</span><span class="sxs-lookup"><span data-stu-id="c75ab-117">After a COM object has been created, you can reference it in subsequent scripts by using the identifier specified in the OBJECT tag's ID attribute.</span></span> <span data-ttu-id="c75ab-118">En el ejemplo anterior, este identificador se especificó como "vid".</span><span class="sxs-lookup"><span data-stu-id="c75ab-118">In the preceding example, this identifier was specified as "vid."</span></span> <span data-ttu-id="c75ab-119">Tenga en cuenta que el script que usa el objeto COM debe aparecer después de la etiqueta de objeto o el script que crea la instancia de objeto. de lo contrario, el identificador de objeto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="c75ab-119">Note that the script that uses the COM object must appear after the OBJECT tag or script that creates the object instance; otherwise, the object identifier is undefined.</span></span> <span data-ttu-id="c75ab-120">En el siguiente script se usa el objeto objXL para mostrar la información de versión de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c75ab-120">The following script uses the objXL object to display the version information for Microsoft Excel.</span></span>

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

<span data-ttu-id="c75ab-121">Si está escribiendo scripts incrustados en una página web, el explorador también expone un modelo de objetos al que pueden tener acceso los scripts.</span><span class="sxs-lookup"><span data-stu-id="c75ab-121">If you are writing scripts embedded in a webpage, the browser also exposes an object model that your scripts can access.</span></span> <span data-ttu-id="c75ab-122">El modelo usado por Internet Explorer se ajusta al Document Object Model (DOM) propuesto por el World Wide Web Consortium (W3C).</span><span class="sxs-lookup"><span data-stu-id="c75ab-122">The model used by Internet Explorer conforms to the Document Object Model (DOM) proposed by the World Wide Web Consortium (W3C).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c75ab-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c75ab-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c75ab-124">Scripting con objetos COM</span><span class="sxs-lookup"><span data-stu-id="c75ab-124">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




