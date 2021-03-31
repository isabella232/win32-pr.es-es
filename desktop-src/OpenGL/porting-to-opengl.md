---
title: Trasladar a OpenGL
description: Trasladar a OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418870"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="194a5-103">Trasladar a OpenGL</span><span class="sxs-lookup"><span data-stu-id="194a5-103">Porting to OpenGL</span></span>

<span data-ttu-id="194a5-104">OpenGL está diseñado para ofrecer compatibilidad entre hardware y sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="194a5-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="194a5-105">Este diseño facilita a los programadores el portabilidad de programas OpenGL de un sistema a otro.</span><span class="sxs-lookup"><span data-stu-id="194a5-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="194a5-106">Aunque cada sistema operativo tiene requisitos únicos, gran parte del código OpenGL de los programas actuales se puede usar tal cual.</span><span class="sxs-lookup"><span data-stu-id="194a5-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="194a5-107">Para trasladar la aplicación de OpenGL a Microsoft Windows, tendrá que modificar los programas para que funcionen con los sistemas de ventanas de Windows.</span><span class="sxs-lookup"><span data-stu-id="194a5-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="194a5-108">En general, las aplicaciones se trasladan a OpenGL para Windows desde una de estas dos plataformas:</span><span class="sxs-lookup"><span data-stu-id="194a5-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="194a5-109">Aplicaciones OpenGL desarrolladas para el sistema de ventanas X y la biblioteca X (Xlib)</span><span class="sxs-lookup"><span data-stu-id="194a5-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="194a5-110">Aplicaciones de contabilidad de IRIS</span><span class="sxs-lookup"><span data-stu-id="194a5-110">IRIS GL applications</span></span>

<span data-ttu-id="194a5-111">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="194a5-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="194a5-112">Introducción a la migración a OpenGL para Windows</span><span class="sxs-lookup"><span data-stu-id="194a5-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="194a5-113">Funciones de OpenGL y sus equivalentes de contabilidad de IRIS</span><span class="sxs-lookup"><span data-stu-id="194a5-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="194a5-114">Diferencias de IRIS GL y OpenGL</span><span class="sxs-lookup"><span data-stu-id="194a5-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




