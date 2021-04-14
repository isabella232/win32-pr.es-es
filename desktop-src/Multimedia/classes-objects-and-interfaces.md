---
title: Clases, objetos e interfaces
description: Clases, objetos e interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488506"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="d5e71-103">Clases, objetos e interfaces</span><span class="sxs-lookup"><span data-stu-id="d5e71-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="d5e71-104">En el lenguaje de programación C++, una *clase* consta de *propiedades* (o datos de miembro) y *métodos* (o funciones miembro).</span><span class="sxs-lookup"><span data-stu-id="d5e71-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="d5e71-105">Las propiedades son elementos de datos, como los contenidos en una estructura.</span><span class="sxs-lookup"><span data-stu-id="d5e71-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="d5e71-106">Los métodos se utilizan para una variedad de propósitos, como la inicialización, la asignación, las operaciones y el acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="d5e71-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="d5e71-107">Se utiliza una declaración de clase de la misma manera que se utiliza una declaración de estructura.</span><span class="sxs-lookup"><span data-stu-id="d5e71-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="d5e71-108">La memoria se asigna a una clase cuando se define un *objeto* de clase.</span><span class="sxs-lookup"><span data-stu-id="d5e71-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="d5e71-109">Cada objeto de clase tiene un área de datos para sus propiedades y una tabla de punteros a los métodos que admite.</span><span class="sxs-lookup"><span data-stu-id="d5e71-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="d5e71-110">En OLE, un objeto consta de datos y métodos, como en C++.</span><span class="sxs-lookup"><span data-stu-id="d5e71-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="d5e71-111">Sin embargo, un objeto OLE cumple las reglas más estrictas.</span><span class="sxs-lookup"><span data-stu-id="d5e71-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="d5e71-112">Los datos son estrictamente internos.</span><span class="sxs-lookup"><span data-stu-id="d5e71-112">The data is strictly internal.</span></span> <span data-ttu-id="d5e71-113">Un objeto solo expone interfaces.</span><span class="sxs-lookup"><span data-stu-id="d5e71-113">An object only exposes interfaces.</span></span> <span data-ttu-id="d5e71-114">Una *interfaz* es un conjunto de métodos relacionados para un objeto.</span><span class="sxs-lookup"><span data-stu-id="d5e71-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="d5e71-115">Cada objeto puede admitir varias interfaces.</span><span class="sxs-lookup"><span data-stu-id="d5e71-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="d5e71-116">Todas las interfaces OLE admiten la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5e71-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




