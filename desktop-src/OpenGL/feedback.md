---
title: Comentarios
description: En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo de comentarios, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678652"
---
# <a name="feedback-mode"></a><span data-ttu-id="5806a-104">Modo de comentarios</span><span class="sxs-lookup"><span data-stu-id="5806a-104">Feedback mode</span></span>

<span data-ttu-id="5806a-105">En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios.</span><span class="sxs-lookup"><span data-stu-id="5806a-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="5806a-106">Suministre esta matriz con [**glFeedbackBuffer**](glfeedbackbuffer.md), que debe llamar antes de colocar OpenGL en modo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="5806a-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="5806a-107">Cada bloque de valores comienza con un código que indica el tipo primitivo, seguido de los valores que describen los vértices del primitivo y los datos asociados.</span><span class="sxs-lookup"><span data-stu-id="5806a-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="5806a-108">Las entradas también se escriben para los mapas de bits y los rectángulos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="5806a-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="5806a-109">No se garantiza que los valores se escriban en la matriz de comentarios hasta que llame a [**glRenderMode**](glrendermode.md) para sacar el modo de comentarios de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5806a-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="5806a-110">Puede usar [**glPassThrough**](glpassthrough.md) para proporcionar un marcador que se devuelve en modo de comentarios como si fuera un primitivo.</span><span class="sxs-lookup"><span data-stu-id="5806a-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




