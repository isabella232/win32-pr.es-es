---
title: Tipos de datos de función y valores devueltos
description: Tipos de datos de función y valores devueltos
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994148"
---
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="b99d2-103">Tipos de datos de función y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b99d2-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="b99d2-104">Las funciones y macros de AVIFile utilizan controladores de archivos y secuencias implementados con la tecnología OLE.</span><span class="sxs-lookup"><span data-stu-id="b99d2-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="b99d2-105">El tipo de datos estándar de una función OLE es **STDAPI** y la función devuelve un valor **HRESULT** (cero si es correcto o un error de lo contrario).</span><span class="sxs-lookup"><span data-stu-id="b99d2-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="b99d2-106">Si una función devuelve un valor distinto de **HRESULT**, el tipo del prototipo de la función tiene una sintaxis ligeramente diferente que incrusta el tipo de valor devuelto entre paréntesis después de "STDAPI \_ ".</span><span class="sxs-lookup"><span data-stu-id="b99d2-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="b99d2-107">Por ejemplo, una función que devuelve un valor de datos **Long** usa **STDAPI \_ (Long)** en la instrucción prototype.</span><span class="sxs-lookup"><span data-stu-id="b99d2-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




