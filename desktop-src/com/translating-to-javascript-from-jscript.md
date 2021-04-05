---
title: Traducir a JavaScript desde JScript
description: Traducir a JavaScript desde JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420367"
---
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="8b910-103">Traducir a JavaScript desde JScript</span><span class="sxs-lookup"><span data-stu-id="8b910-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="8b910-104">JScript es compatible en gran medida con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8b910-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="8b910-105">Sin embargo, JScript incluye algunos objetos que no son compatibles actualmente con JavaScript, como ActiveXObject, Enumerator, error, global y VBArray.</span><span class="sxs-lookup"><span data-stu-id="8b910-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="8b910-106">La versión 5,0 de JScript admite el control de excepciones mediante **try**... instrucciones **catch** .</span><span class="sxs-lookup"><span data-stu-id="8b910-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="8b910-107">JavaScript no proporciona actualmente un mecanismo de control de errores.</span><span class="sxs-lookup"><span data-stu-id="8b910-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="8b910-108">Al trabajar con JScript o JavaScript, existen algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores Web.</span><span class="sxs-lookup"><span data-stu-id="8b910-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="8b910-109">Para escribir un script que se ejecute en Internet Explorer y en Netscape Navigator, limite las características que usan los scripts a las que se especifican en el estándar de World Wide Web Consortium (W3C) [para la versión 3,2 de HTML](https://www.w3.org/tr/rec-html32.html).</span><span class="sxs-lookup"><span data-stu-id="8b910-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b910-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b910-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b910-111">Traducir a JavaScript</span><span class="sxs-lookup"><span data-stu-id="8b910-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




