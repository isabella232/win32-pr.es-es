---
title: Traducir a JScript desde VBScript
description: Traducir a JScript desde VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773567"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="1a927-103">Traducir a JScript desde VBScript</span><span class="sxs-lookup"><span data-stu-id="1a927-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="1a927-104">En VBScript, la **de**... **Cada** bucle enumera los miembros de una colección; en JScript, la **para**... **in** Loop enumera los miembros de un objeto o una matriz de JScript.</span><span class="sxs-lookup"><span data-stu-id="1a927-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="1a927-105">Para enumerar una colección en JScript, use un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="1a927-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="1a927-106">En JScript, hay varios tipos de datos, como números, cadenas, valores booleanos, objetos y el atributo null.</span><span class="sxs-lookup"><span data-stu-id="1a927-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="1a927-107">VBScript solo utiliza un tipo de datos, **Variant**, que se puede subescribir para representar cadenas, números, valores booleanos, etc.</span><span class="sxs-lookup"><span data-stu-id="1a927-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="1a927-108">En JScript, las matrices se pueden expandir dinámicamente estableciendo un nuevo valor para la propiedad Length de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1a927-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="1a927-109">En VBScript, no se pueden ampliar las matrices; se deben redimensionar con la instrucción **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="1a927-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="1a927-110">Tanto VBScript como JScript admiten funciones.</span><span class="sxs-lookup"><span data-stu-id="1a927-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="1a927-111">Sin embargo, VBScript también admite subrutinas.</span><span class="sxs-lookup"><span data-stu-id="1a927-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="1a927-112">Las subrutinas son similares a las funciones, pero no devuelven un valor.</span><span class="sxs-lookup"><span data-stu-id="1a927-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="1a927-113">JScript distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1a927-113">JScript is case-sensitive.</span></span> <span data-ttu-id="1a927-114">VBScript no lo es.</span><span class="sxs-lookup"><span data-stu-id="1a927-114">VBScript is not.</span></span>

<span data-ttu-id="1a927-115">JScript es compatible con Internet Explorer y Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="1a927-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="1a927-116">Netscape Navigator no es compatible con VBScript.</span><span class="sxs-lookup"><span data-stu-id="1a927-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="1a927-117">JScript proporciona el objeto de error, que se puede utilizar para interceptar y controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="1a927-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="1a927-118">El objeto error es análogo al objeto Err de VBScript.</span><span class="sxs-lookup"><span data-stu-id="1a927-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="1a927-119">Las matrices de JScript no son matrices del tipo de variable **Variant SafeArray**.</span><span class="sxs-lookup"><span data-stu-id="1a927-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="1a927-120">Si el script recibe una variable **Variant de tipo SafeArray** de un objeto com o un script de VBScript, debe utilizar un objeto VBArray para tener acceso a la variable de **tipo SafeArray** de la variante.</span><span class="sxs-lookup"><span data-stu-id="1a927-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a927-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a927-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a927-122">Traducir a JScript</span><span class="sxs-lookup"><span data-stu-id="1a927-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




