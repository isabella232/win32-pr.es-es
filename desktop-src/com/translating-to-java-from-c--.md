---
title: Traducir a Java desde C++
description: Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Java, los punteros se controlan automáticamente.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418415"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="f6fec-105">Traducir a Java desde C++</span><span class="sxs-lookup"><span data-stu-id="f6fec-105">Translating to Java from C++</span></span>

<span data-ttu-id="f6fec-106">Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada.</span><span class="sxs-lookup"><span data-stu-id="f6fec-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="f6fec-107">Los punteros de memoria proporcionan este acceso directo.</span><span class="sxs-lookup"><span data-stu-id="f6fec-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="f6fec-108">En Java, los punteros se controlan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f6fec-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="f6fec-109">En Java, los tipos de datos compuestos **struct**, **Union** y **typedef** se controlan exclusivamente mediante el uso de clases.</span><span class="sxs-lookup"><span data-stu-id="f6fec-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="f6fec-110">Por ejemplo, el tipo de datos **Variant** de C++ se asigna a **com. ms. com. Variant** en Java.</span><span class="sxs-lookup"><span data-stu-id="f6fec-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="f6fec-111">En C++, las cadenas son una matriz de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f6fec-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="f6fec-112">En Java, las cadenas son objetos.</span><span class="sxs-lookup"><span data-stu-id="f6fec-112">In Java, strings are objects.</span></span> <span data-ttu-id="f6fec-113">Los métodos que actúan en cadenas tratan la cadena como un objeto completo.</span><span class="sxs-lookup"><span data-stu-id="f6fec-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="f6fec-114">Los métodos COM devuelven un valor conocido como **HRESULT**, que es un código de error de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f6fec-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="f6fec-115">La compatibilidad de Java con Microsoft Internet Explorer define una clase, **com. ms. com. COMException**, que contiene el código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6fec-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="f6fec-116">Java no admite tipos de datos sin signo excepto **Char**, que es un entero sin signo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f6fec-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="f6fec-117">Los métodos que aceptan o devuelven otros tipos de datos sin signo no se pueden usar desde Java.</span><span class="sxs-lookup"><span data-stu-id="f6fec-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="f6fec-118">Java no admite matrices multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="f6fec-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="f6fec-119">Los métodos que aceptan o devuelven matrices multidimensionales no están disponibles en Java.</span><span class="sxs-lookup"><span data-stu-id="f6fec-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="f6fec-120">Los valores booleanos de Java no se pueden convertir a 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="f6fec-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6fec-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6fec-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6fec-122">Traducir a Java</span><span class="sxs-lookup"><span data-stu-id="f6fec-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




