---
description: Notación de objetos JavaScript (JSON)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: Notación de objetos JavaScript (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b5f12a2c4e3a4cd0a66a8f917c3cdf41ed17d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088193"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="f7c06-103">Notación de objetos JavaScript (JSON)</span><span class="sxs-lookup"><span data-stu-id="f7c06-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="f7c06-104">[notación de objetos JavaScript (JSON)](https://www.json.org/) es un formato de intercambio de datos sencillo y ligero que se basa en un subconjunto de la notación literal de objeto del lenguaje JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f7c06-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="f7c06-105">El motor de JavaScript de Windows Internet Explorer 8 implementa la propuesta [DE JSON de ECMAScript 3.1](https://www.ecma-international.org/) para funciones nativas de control de JSON (que usa la API de json2.js [de Douglas Crockford).](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)</span><span class="sxs-lookup"><span data-stu-id="f7c06-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="f7c06-106">Internet Explorer 8 incluye un objeto JSON nativo que cumple con la compatibilidad con JSON que se describe en el borrador de trabajo de propuestas [de ES3.1](https://www.ecma-international.org/).</span><span class="sxs-lookup"><span data-stu-id="f7c06-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="f7c06-107">Algunas páginas web detectan el objeto JSON nativo y, a continuación, lo usan de forma no estándar.</span><span class="sxs-lookup"><span data-stu-id="f7c06-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="f7c06-108">Este uso suele provocar un error de script e interrumpe el control de las solicitudes AJAX.</span><span class="sxs-lookup"><span data-stu-id="f7c06-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="f7c06-109">En el ejemplo de código siguiente se muestra la manera incorrecta de usar el objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f7c06-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="f7c06-110">En su lugar, en el ejemplo de código siguiente se muestra una buena manera de usar el objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f7c06-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="f7c06-111">Windows Internet Explorer compatibilidad nativa con JSON mediante la introducción de un objeto JSON global que tiene dos métodos integrados: **stringify** **y parse**.</span><span class="sxs-lookup"><span data-stu-id="f7c06-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="f7c06-112">El objeto JSON global se define en el motor de JavaScript y se crea durante la fase de inicialización del motor.</span><span class="sxs-lookup"><span data-stu-id="f7c06-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="f7c06-113">Para mantener la compatibilidad con versiones anteriores, esta característica solo está disponible cuando un sitio web usa la versión más reciente de las características de JavaScript mediante el modo de diseño "Internet Explorer 8 Estándares" (documento).</span><span class="sxs-lookup"><span data-stu-id="f7c06-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="f7c06-114">Esta característica también puede afectar al comportamiento de las páginas web que dependen de una variable global JSON o usan [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="f7c06-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="f7c06-115">Puede invalidar el objeto JSON global.</span><span class="sxs-lookup"><span data-stu-id="f7c06-115">You can override the global JSON object.</span></span> <span data-ttu-id="f7c06-116">Pero cuando una página web usa el modo de diseño "Internet Explorer 8 Estándares" (documento), ya no es un objeto indefinido.</span><span class="sxs-lookup"><span data-stu-id="f7c06-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="f7c06-117">Dado que el motor de JavaScript crea instancias de JSON como un nombre global, las comprobaciones como "if(!this.JSON)" se evalúan como False y deben cambiarse en el código de usuario.</span><span class="sxs-lookup"><span data-stu-id="f7c06-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="f7c06-118">Las páginas web que [ usanjson2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) probablemente no se verán afectadas.</span><span class="sxs-lookup"><span data-stu-id="f7c06-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="f7c06-119">Con pocas excepciones, estas páginas deberían funcionar más rápido.</span><span class="sxs-lookup"><span data-stu-id="f7c06-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="f7c06-120">Las excepciones se debe a las diferencias entre la implementación Internet Explorer JSON nativa y json2.js.</span><span class="sxs-lookup"><span data-stu-id="f7c06-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="f7c06-121">Por ejemplo, durante la serialización, la implementación json nativa detecta ciclos y no entra en recursividad infinita como json.js.</span><span class="sxs-lookup"><span data-stu-id="f7c06-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="f7c06-122">Para obtener más información sobre estas excepciones, vea los [blogs de JavaScript](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="f7c06-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="f7c06-123">Para más información, consulte [Documentación y](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) control de versiones de JSON y Compatibilidad con versiones del motor de [JavaScript.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c06-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7c06-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7c06-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7c06-125">Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="f7c06-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
