---
title: Traducir a C++ desde Visual Basic
description: Visual Basic controla los punteros implícitamente. En C++, la aplicación es responsable de realizar cualquier aritmética de puntero necesaria.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268733"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="68d08-104">Traducir a C++ desde Visual Basic</span><span class="sxs-lookup"><span data-stu-id="68d08-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="68d08-105">Visual Basic controla los punteros implícitamente.</span><span class="sxs-lookup"><span data-stu-id="68d08-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="68d08-106">En C++, la aplicación es responsable de realizar cualquier aritmética de puntero necesaria.</span><span class="sxs-lookup"><span data-stu-id="68d08-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="68d08-107">De forma predeterminada, Visual Basic pasa los parámetros por referencia (como punteros).</span><span class="sxs-lookup"><span data-stu-id="68d08-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="68d08-108">Los parámetros que se deben pasar por valor solo se especifican mediante la palabra clave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="68d08-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="68d08-109">Por ejemplo, un **parámetro ByVal** â  **integer** en Visual Basic es equivalente a un **parámetro Short** en C++, mientras que un parámetro de  **tipo entero** **ByRef** en Visual Basic es equivalente a un parámetro **Short \*** .</span><span class="sxs-lookup"><span data-stu-id="68d08-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="68d08-110">Un parámetro declarado **como String** en Visual Basic se declara como un puntero a un **BSTR** en C++.</span><span class="sxs-lookup"><span data-stu-id="68d08-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="68d08-111">Establecer un puntero de cadena en **null** en C++ es equivalente a establecer la cadena en la constante **vbNullString** en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="68d08-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="68d08-112">Pasar una cadena de longitud cero ("") a una función diseñada para recibir **null** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de un puntero cero.</span><span class="sxs-lookup"><span data-stu-id="68d08-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="68d08-113">C++ y Visual Basic difieren ligeramente en la forma en que representan las propiedades.</span><span class="sxs-lookup"><span data-stu-id="68d08-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="68d08-114">En C++, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="68d08-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="68d08-115">En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="68d08-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d08-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68d08-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d08-117">Traducir a C++</span><span class="sxs-lookup"><span data-stu-id="68d08-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




