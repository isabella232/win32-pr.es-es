---
title: Trasladar a Java desde Visual Basic
description: Trasladar a Java desde Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418414"
---
# <a name="translating-to-java-from-visual-basic"></a><span data-ttu-id="bfb17-103">Trasladar a Java desde Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bfb17-103">Translating to Java from Visual Basic</span></span>

<span data-ttu-id="bfb17-104">De forma predeterminada, Visual Basic pasa los parámetros por referencia.</span><span class="sxs-lookup"><span data-stu-id="bfb17-104">By default, Visual Basic passes parameters by reference.</span></span> <span data-ttu-id="bfb17-105">Los parámetros que se deben pasar por valor solo se especifican mediante la palabra clave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="bfb17-105">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span>

<span data-ttu-id="bfb17-106">Java no admite matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="bfb17-106">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="bfb17-107">Los métodos que aceptan o devuelven matrices multidimensionales no están disponibles en Java.</span><span class="sxs-lookup"><span data-stu-id="bfb17-107">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="bfb17-108">Java y Visual Basic difieren ligeramente en cómo representan las propiedades.</span><span class="sxs-lookup"><span data-stu-id="bfb17-108">Java and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="bfb17-109">En Java, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bfb17-109">In Java, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="bfb17-110">En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bfb17-110">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfb17-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfb17-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfb17-112">Traducir a Java</span><span class="sxs-lookup"><span data-stu-id="bfb17-112">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




