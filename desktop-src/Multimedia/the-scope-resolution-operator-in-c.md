---
title: Operador de resolución de ámbito en C++
description: Operador de resolución de ámbito en C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903503"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="830c8-103">Operador de resolución de ámbito en C++</span><span class="sxs-lookup"><span data-stu-id="830c8-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="830c8-104">Dos puntos (::) se usan en C++ como un operador de *resolución de ámbito* .</span><span class="sxs-lookup"><span data-stu-id="830c8-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="830c8-105">Este operador proporciona más libertad para asignar nombres a las variables, ya que permite distinguir entre las variables con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="830c8-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="830c8-106">Por ejemplo, mi *archivo:: Read* hace referencia al *método Read* *de la clase* de objetos YourFile, en lugar de a *:: Read*, que hace referencia a un método *Read* de la clase *YourFile* .</span><span class="sxs-lookup"><span data-stu-id="830c8-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




