---
title: Traducir a JavaScript desde VBScript
description: Traducir a JavaScript desde VBScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356766"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="c7376-103">Traducir a JavaScript desde VBScript</span><span class="sxs-lookup"><span data-stu-id="c7376-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="c7376-104">En JavaScript, hay varios tipos de datos, como números, cadenas, booleanos, objetos y el atributo null.</span><span class="sxs-lookup"><span data-stu-id="c7376-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="c7376-105">VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.</span><span class="sxs-lookup"><span data-stu-id="c7376-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="c7376-106">En JavaScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c7376-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="c7376-107">En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="c7376-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="c7376-108">Tanto VBScript como JavaScript admiten funciones.</span><span class="sxs-lookup"><span data-stu-id="c7376-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="c7376-109">Sin embargo, VBScript también admite subrutinas.</span><span class="sxs-lookup"><span data-stu-id="c7376-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="c7376-110">Las subrutinas son similares a las funciones, pero no devuelven un valor.</span><span class="sxs-lookup"><span data-stu-id="c7376-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="c7376-111">JavaScript distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7376-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="c7376-112">VBScript no lo es.</span><span class="sxs-lookup"><span data-stu-id="c7376-112">VBScript is not.</span></span>

<span data-ttu-id="c7376-113">JavaScript es compatible con una amplia variedad de exploradores Web, incluidos Internet Explorer y Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="c7376-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="c7376-114">VBScript solo es compatible con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c7376-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="c7376-115">VBScript proporciona compatibilidad de control de errores a través de su objeto Err.</span><span class="sxs-lookup"><span data-stu-id="c7376-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="c7376-116">JavaScript no proporciona actualmente un medio para interceptar y controlar errores.</span><span class="sxs-lookup"><span data-stu-id="c7376-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7376-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7376-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7376-118">Traducir a JavaScript</span><span class="sxs-lookup"><span data-stu-id="c7376-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




