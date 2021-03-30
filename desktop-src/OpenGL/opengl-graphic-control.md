---
title: Control gráfico OpenGL
description: Control gráfico OpenGL
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, control gráfico
- control gráfico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776135"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="12706-105">Control gráfico OpenGL</span><span class="sxs-lookup"><span data-stu-id="12706-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="12706-106">OpenGL proporciona un control bastante directo sobre las operaciones fundamentales de los gráficos de dos y tres dimensiones.</span><span class="sxs-lookup"><span data-stu-id="12706-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="12706-107">Esto incluye la especificación de estos parámetros como matrices de transformación, los coeficientes de ecuaciones de iluminación, los métodos de suavizado de contorno y los operadores de actualización de píxeles.</span><span class="sxs-lookup"><span data-stu-id="12706-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="12706-108">Sin embargo, no proporciona un medio para describir o modelar objetos geométricos complejos.</span><span class="sxs-lookup"><span data-stu-id="12706-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="12706-109">Por lo tanto, los comandos OpenGL que emita especifican cómo se debe generar un determinado resultado (el procedimiento que debe seguirse) en lugar de lo que debe ser exactamente el resultado.</span><span class="sxs-lookup"><span data-stu-id="12706-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="12706-110">Es decir, OpenGL es fundamentalmente procedimental en lugar de descriptivo.</span><span class="sxs-lookup"><span data-stu-id="12706-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="12706-111">Para entender completamente cómo usar OpenGL, ayuda a conocer el orden en el que lleva a cabo sus operaciones.</span><span class="sxs-lookup"><span data-stu-id="12706-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




