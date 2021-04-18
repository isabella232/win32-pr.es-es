---
title: Control de errores (OpenGL)
description: Cuando OpenGL detecta un error, registra un código de error actual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- control de errores OpenGL
- Control de errores de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676542"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="24df2-105">Control de errores (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="24df2-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="24df2-106">Cuando OpenGL detecta un error, registra un código de error actual.</span><span class="sxs-lookup"><span data-stu-id="24df2-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="24df2-107">La función que causó el error se omite, por lo que no tiene ningún efecto en el estado de OpenGL o en el contenido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="24df2-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="24df2-108">(Si el error registrado es GL \_ \_ \_ Sin embargo, los resultados de la función no están definidos. Una vez registrado, el código de error actual no se borra hasta que se llama a la función de consulta [**glGetError**](glgeterror.md) , que devuelve el código de error actual.</span><span class="sxs-lookup"><span data-stu-id="24df2-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="24df2-109">Las implementaciones de OpenGL pueden devolver varios códigos de error actuales, cada uno de los cuales permanece establecido hasta que se consultan.</span><span class="sxs-lookup"><span data-stu-id="24df2-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="24df2-110">La función **glGetError** devuelve GL \_ no \_ error una vez que ha consultado todos los códigos de error actuales o si no hay ningún error.</span><span class="sxs-lookup"><span data-stu-id="24df2-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="24df2-111">Por lo tanto, si obtiene un código de error, llame a **glGetError** hasta que \_ no \_ se devuelva ningún error para asegurarse de que ha detectado todos los errores.</span><span class="sxs-lookup"><span data-stu-id="24df2-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="24df2-112">Para obtener la lista de códigos de error, consulte [códigos de error de OpenGL](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="24df2-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="24df2-113">Puede usar la función [**gluErrorString**](gluerrorstring.md) Glu para obtener una cadena descriptiva correspondiente al código de error que se pasa.</span><span class="sxs-lookup"><span data-stu-id="24df2-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="24df2-114">Para obtener más información sobre **gluErrorString**, consulte [control de errores](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="24df2-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="24df2-115">Las funciones GLU a menudo devuelven valores de error si se detecta un error.</span><span class="sxs-lookup"><span data-stu-id="24df2-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="24df2-116">Además, la biblioteca de la utilidad OpenGL define los códigos de error GLU \_ \_ enumeración no válida, Glu \_ valor no válido \_ y Glu \_ memoria insuficiente \_ \_ , que tienen el mismo significado que los códigos de error de OpenGL relacionados.</span><span class="sxs-lookup"><span data-stu-id="24df2-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




