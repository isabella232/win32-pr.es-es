---
title: Conceptos de programación de C++ y OLE
description: Conceptos de programación de C++ y OLE
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903874"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="3297c-103">Conceptos de programación de C++ y OLE</span><span class="sxs-lookup"><span data-stu-id="3297c-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="3297c-104">Los controladores de archivos y secuencias incluidos con Windows usan un diseño orientado a objetos para promocionar una interfaz estándar y compartir la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3297c-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="3297c-105">Estos controladores se escriben en C++ y utilizan el modelo de objetos de componentes OLE.</span><span class="sxs-lookup"><span data-stu-id="3297c-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="3297c-106">Puede desarrollar controladores personalizados mediante los sistemas de desarrollo de C o C++; sin embargo, se recomienda encarecidamente el uso de C++, ya que proporciona un enfoque más sencillo y sencillo para implementar un controlador.</span><span class="sxs-lookup"><span data-stu-id="3297c-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="3297c-107">Con C++, puede definir explícitamente los datos como objetos y puede asociar las funciones que manipulan los datos con las funciones miembro de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3297c-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="3297c-108">En esta sección se identifican y resumen brevemente los conceptos importantes de C++ y el modelo de objetos de componentes OLE que se aplican al diseño y la implementación de controladores de archivos y secuencias.</span><span class="sxs-lookup"><span data-stu-id="3297c-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="3297c-109">Hay muchos libros escritos sobre la programación de C++ a los que puede hacer referencia para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3297c-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="3297c-110">Para obtener más información sobre OLE, vea la *Referencia del programador de OLE*.</span><span class="sxs-lookup"><span data-stu-id="3297c-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




