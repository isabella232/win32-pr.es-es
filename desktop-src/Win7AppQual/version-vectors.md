---
description: Un vector de versión procesa los comentarios condicionales en una página web HTML. Es decir, los vectores de versión permiten crear el marcado en función de la versión del explorador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vectores de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361708"
---
# <a name="version-vectors"></a><span data-ttu-id="11674-104">Vectores de versión</span><span class="sxs-lookup"><span data-stu-id="11674-104">Version Vectors</span></span>

<span data-ttu-id="11674-105">Un *Vector de versión* procesa los comentarios condicionales en una página web HTML.</span><span class="sxs-lookup"><span data-stu-id="11674-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="11674-106">Es decir, los vectores de versión permiten crear el marcado en función de la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="11674-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="11674-107">Tenga en cuenta el siguiente código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="11674-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="11674-108">En este caso, si la versión del explorador de Windows Internet Explorer es al menos 5,5, el párrafo correspondiente se muestra en la Página Web.</span><span class="sxs-lookup"><span data-stu-id="11674-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="11674-109">Aunque la primera condición de este ejemplo muestra la función de los comentarios condicionales, estos comentarios no se suelen usar para mostrar el marcado como la primera condición.</span><span class="sxs-lookup"><span data-stu-id="11674-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="11674-110">En su lugar, los comentarios condicionales restantes en el ejemplo anterior son más comunes.</span><span class="sxs-lookup"><span data-stu-id="11674-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="11674-111">En estos comentarios restantes, los comentarios condicionales usan una hoja de estilos diferente para cada versión diferente del explorador.</span><span class="sxs-lookup"><span data-stu-id="11674-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="11674-112">En el ejemplo de código anterior también se comprueba la igualdad de Microsoft Internet Explorer 6 y Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="11674-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="11674-113">Pero para Windows Internet Explorer 8, el ejemplo utiliza el operador de GTE (mayor o igual que).</span><span class="sxs-lookup"><span data-stu-id="11674-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="11674-114">Este operador ayuda a probar en el futuro el ejemplo para que se use la versión más conforme a los estándares de la hoja de estilos cuando se lance una nueva versión del explorador (en lugar de usar la hoja de estilos equivocada o ninguna hoja de estilos).</span><span class="sxs-lookup"><span data-stu-id="11674-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="11674-115">Las aplicaciones existentes no suelen tener en cuenta una versión de Internet Explorer anterior 7 (o la versión más reciente de Internet Explorer para la que se ha creado el sitio).</span><span class="sxs-lookup"><span data-stu-id="11674-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="11674-116">Para obtener más información acerca de los vectores de versión, consulte [vectores de versión](/previous-versions/cc817577(v=msdn.10)) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="11674-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11674-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11674-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11674-118">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="11674-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



