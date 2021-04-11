---
title: Usar JavaScript y JScript
description: Usar JavaScript y JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149248"
---
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="f980e-103">Usar JavaScript y JScript</span><span class="sxs-lookup"><span data-stu-id="f980e-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="f980e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f980e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f980e-105">Si usa JavaScript o Microsoft JScript para tener acceso a la interfaz de programación de Microsoft Agent, siga las convenciones de este lenguaje para especificar métodos o propiedades:</span><span class="sxs-lookup"><span data-stu-id="f980e-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="f980e-106">JavaScript no tiene actualmente sintaxis de eventos para objetos no HTML.</span><span class="sxs-lookup"><span data-stu-id="f980e-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="f980e-107">Sin embargo, con Internet Explorer puede usar la `<SCRIPT>` etiqueta **for...** Sintaxis del evento:</span><span class="sxs-lookup"><span data-stu-id="f980e-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="f980e-108">Dado que no todos los exploradores admiten actualmente esta sintaxis de eventos, puede que desee usar JavaScript solo para las páginas que admiten Microsoft Internet Explorer o para el código que no requiere el control de eventos.</span><span class="sxs-lookup"><span data-stu-id="f980e-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="f980e-109">Para obtener acceso a las colecciones de objetos del agente, utilice la función de [**enumerador**](https://www.bing.com/search?q=**Enumerator**) de JScript.</span><span class="sxs-lookup"><span data-stu-id="f980e-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="f980e-110">Sin embargo, las versiones de JScript incluidas antes de Internet Explorer 4,0 no admiten esta función y no admiten colecciones.</span><span class="sxs-lookup"><span data-stu-id="f980e-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="f980e-111">Para tener acceso a los métodos y las propiedades del objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) , utilice el método de [**caracteres**](character-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f980e-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="f980e-112">Del mismo modo, para obtener acceso a las propiedades de un objeto [**Command**](/windows/desktop/lwef/the-command-object) , use el método [**Command**](command-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f980e-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 