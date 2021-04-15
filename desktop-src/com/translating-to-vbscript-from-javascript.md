---
title: Traducir a VBScript desde JavaScript
description: Traducir a VBScript desde JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714145"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="400bf-103">Traducir a VBScript desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="400bf-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="400bf-104">En JavaScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null.</span><span class="sxs-lookup"><span data-stu-id="400bf-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="400bf-105">VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.</span><span class="sxs-lookup"><span data-stu-id="400bf-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="400bf-106">En JavaScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz.</span><span class="sxs-lookup"><span data-stu-id="400bf-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="400bf-107">En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="400bf-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="400bf-108">Tanto VBScript como JavaScript admiten funciones.</span><span class="sxs-lookup"><span data-stu-id="400bf-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="400bf-109">Sin embargo, VBScript también admite subrutinas.</span><span class="sxs-lookup"><span data-stu-id="400bf-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="400bf-110">Las subrutinas son similares a las funciones, salvo que no devuelven un valor.</span><span class="sxs-lookup"><span data-stu-id="400bf-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="400bf-111">JavaScript distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="400bf-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="400bf-112">VBScript no lo es.</span><span class="sxs-lookup"><span data-stu-id="400bf-112">VBScript is not.</span></span>

<span data-ttu-id="400bf-113">JavaScript es compatible con una amplia variedad de exploradores Web, incluidos Internet Explorer y Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="400bf-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="400bf-114">Netscape Navigator no es compatible con VBScript.</span><span class="sxs-lookup"><span data-stu-id="400bf-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="400bf-115">VBScript admite el control de errores a través de su objeto Err.</span><span class="sxs-lookup"><span data-stu-id="400bf-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="400bf-116">JavaScript no proporciona actualmente un medio para interceptar y controlar errores.</span><span class="sxs-lookup"><span data-stu-id="400bf-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="400bf-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="400bf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="400bf-118">Traducir a VBScript</span><span class="sxs-lookup"><span data-stu-id="400bf-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




