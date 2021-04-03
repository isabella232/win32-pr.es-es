---
title: Traducir a VBScript desde JScript
description: Traducir a VBScript desde JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075412"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="c102f-103">Traducir a VBScript desde JScript</span><span class="sxs-lookup"><span data-stu-id="c102f-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="c102f-104">En VBScript, la **de**... **Cada** bucle enumera los miembros de una colección; en JScript, la **para**... **in** Loop enumera los miembros de un objeto o una matriz de JScript.</span><span class="sxs-lookup"><span data-stu-id="c102f-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="c102f-105">Para enumerar una colección en JScript, use un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="c102f-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="c102f-106">JScript proporciona el objeto de error, que se puede utilizar para interceptar y controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="c102f-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="c102f-107">El objeto error es análogo al objeto Err de VBScript.</span><span class="sxs-lookup"><span data-stu-id="c102f-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="c102f-108">En JScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null.</span><span class="sxs-lookup"><span data-stu-id="c102f-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="c102f-109">VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.</span><span class="sxs-lookup"><span data-stu-id="c102f-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="c102f-110">En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c102f-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="c102f-111">En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="c102f-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="c102f-112">Tanto VBScript como JScript admiten funciones.</span><span class="sxs-lookup"><span data-stu-id="c102f-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="c102f-113">Sin embargo, VBScript también admite subrutinas.</span><span class="sxs-lookup"><span data-stu-id="c102f-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="c102f-114">Las subrutinas son similares a las funciones, pero no devuelven un valor.</span><span class="sxs-lookup"><span data-stu-id="c102f-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="c102f-115">JScript distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c102f-115">JScript is case-sensitive.</span></span> <span data-ttu-id="c102f-116">VBScript no lo es.</span><span class="sxs-lookup"><span data-stu-id="c102f-116">VBScript is not.</span></span>

<span data-ttu-id="c102f-117">JScript es compatible con una amplia variedad de exploradores Web, incluidos Internet Explorer y Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="c102f-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="c102f-118">Netscape Navigator no es compatible con VBScript.</span><span class="sxs-lookup"><span data-stu-id="c102f-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="c102f-119">Las matrices de JScript no son matrices del tipo de variable **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="c102f-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="c102f-120">Un script de JScript debe utilizar un objeto VBArray para tener acceso a la variable **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="c102f-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="c102f-121">Los scripts de VBScript pueden tener acceso directamente a las variables **SAFEARRAY de variante**.</span><span class="sxs-lookup"><span data-stu-id="c102f-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c102f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c102f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c102f-123">Traducir a VBScript</span><span class="sxs-lookup"><span data-stu-id="c102f-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




