---
description: Descripción de los conflictos entre los movimientos de aplicación y los caracteres y símbolos.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflictos entre los gestos y caracteres y símbolos de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714959"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a><span data-ttu-id="b6906-103">Conflictos entre los gestos y caracteres y símbolos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b6906-103">Conflicts Between Application Gestures and Characters and Symbols</span></span>

<span data-ttu-id="b6906-104">Algunos gestos de la aplicación pueden entrar en conflicto con caracteres, combinaciones de caracteres, símbolos, combinaciones de caracteres y símbolos o palabras completas escritas en un solo trazo.</span><span class="sxs-lookup"><span data-stu-id="b6906-104">Some application gestures may conflict with characters, combinations of characters, symbols, combinations of characters and symbols or whole words written in a single stroke.</span></span> <span data-ttu-id="b6906-105">La mayoría de estos conflictos se evitan al tener un conocimiento detallado del contexto en el que se realiza el gesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6906-105">Most of these conflicts are avoided by having a detailed understanding of the context in which the application gesture is performed.</span></span>

<span data-ttu-id="b6906-106">Por ejemplo, para distinguir un gesto correcto de un guión (-) o un carácter de subrayado ( \_ ), una aplicación puede filtrar el cierre de los caracteres contiguos, el tamaño relativo en comparación con los caracteres u otra información contenida en un paquete.</span><span class="sxs-lookup"><span data-stu-id="b6906-106">For example, to distinguish a right gesture from a dash (-) or an underscore (\_), an application may filter for how close the gesture is to neighboring characters, the relative size as compared to characters, or other information contained in a packet.</span></span> <span data-ttu-id="b6906-107">El tiempo del gesto de aplicación también puede ser un factor determinante a la hora de decidir entre los gestos y los caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6906-107">The timing of the application gesture may also be a determining factor in deciding between gestures and characters.</span></span> <span data-ttu-id="b6906-108">Puede haber más de una pausa antes de aplicar un gesto de aplicación que antes de introducir caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6906-108">There may be more of a pause before applying an application gesture than before inputting characters.</span></span> <span data-ttu-id="b6906-109">A menos que un usuario realice una serie de movimientos de deshacer o de retroceso, también puede haber más de una pausa después de un movimiento que un carácter.</span><span class="sxs-lookup"><span data-stu-id="b6906-109">Unless a user is performing a series of undo or backspace gestures, there may also be more of a pause after a gesture than a character.</span></span>

<span data-ttu-id="b6906-110">En los temas siguientes se detallan estos conflictos:</span><span class="sxs-lookup"><span data-stu-id="b6906-110">The following topics detail these conflicts:</span></span>

-   [<span data-ttu-id="b6906-111">Conflictos con caracteres latinos y símbolos</span><span class="sxs-lookup"><span data-stu-id="b6906-111">Conflicts with Latin characters and symbols</span></span>](conflicts-with-latin-characters-and-symbols.md)
-   [<span data-ttu-id="b6906-112">Conflictos con caracteres de East-Asian</span><span class="sxs-lookup"><span data-stu-id="b6906-112">Conflicts with East-Asian Characters</span></span>](conflicts-with-east-asian-characters.md)

 

 



