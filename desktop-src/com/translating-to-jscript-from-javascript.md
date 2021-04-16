---
title: Traducir a JScript desde JavaScript
description: Traducir a JScript desde JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533027"
---
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="452dd-103">Traducir a JScript desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="452dd-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="452dd-104">JScript es compatible en gran medida con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="452dd-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="452dd-105">Sin embargo, JScript versión 5,0 incluye algunos objetos que no admite actualmente JavaScript, como ActiveXObject, Enumerator, error, global y VBArray.</span><span class="sxs-lookup"><span data-stu-id="452dd-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="452dd-106">JScript 5,0 admite el control de excepciones mediante **try**... instrucciones **catch** .</span><span class="sxs-lookup"><span data-stu-id="452dd-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="452dd-107">JavaScript no proporciona actualmente un mecanismo de control de errores.</span><span class="sxs-lookup"><span data-stu-id="452dd-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="452dd-108">Al trabajar con JScript o JavaScript, existen algunas diferencias sutiles entre las implementaciones del modelo de objetos compatibles con varios exploradores Web.</span><span class="sxs-lookup"><span data-stu-id="452dd-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="452dd-109">Para escribir un script que se ejecute en Internet Explorer y en Netscape Navigator, limite las características que usan los scripts a las que se especifican en el estándar de World Wide Web Consortium (W3C) para la versión 3,2 de HTML.</span><span class="sxs-lookup"><span data-stu-id="452dd-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="452dd-110">Para obtener más información acerca de este estándar, consulte [especificación de referencia de HTML 3,2](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="452dd-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="452dd-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="452dd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="452dd-112">Traducir a JScript</span><span class="sxs-lookup"><span data-stu-id="452dd-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




