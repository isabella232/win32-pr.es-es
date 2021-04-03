---
title: Crear un controlador de archivo o secuencia
description: Crear un controlador de archivo o secuencia
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075587"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="92e86-103">Crear un controlador de archivo o secuencia</span><span class="sxs-lookup"><span data-stu-id="92e86-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="92e86-104">En una aplicación escrita en el lenguaje de programación C, un controlador de archivo o secuencia normalmente crea una función para cada método.</span><span class="sxs-lookup"><span data-stu-id="92e86-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="92e86-105">La aplicación tiene acceso a estas funciones a través de una matriz de punteros de función que crea el controlador de flujo.</span><span class="sxs-lookup"><span data-stu-id="92e86-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="92e86-106">Una estructura **IAVIStreamVtbl** contiene la matriz de punteros de función.</span><span class="sxs-lookup"><span data-stu-id="92e86-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="92e86-107">Un controlador de flujo puede asignar cualquier nombre que desee a las funciones que crea para los métodos.</span><span class="sxs-lookup"><span data-stu-id="92e86-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="92e86-108">La posición del puntero de función en la estructura implica la correspondencia de la función con el método.</span><span class="sxs-lookup"><span data-stu-id="92e86-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="92e86-109">Por ejemplo, el primer puntero de función de la estructura corresponde al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="92e86-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="92e86-110">El controlador de flujo debe proporcionar todas las funciones de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="92e86-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




