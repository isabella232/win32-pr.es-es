---
description: Información general sobre el registro de errores
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Información general sobre el registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152285"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="0daeb-103">Información general sobre el registro de errores</span><span class="sxs-lookup"><span data-stu-id="0daeb-103">Overview of Error Logging</span></span>

<span data-ttu-id="0daeb-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="0daeb-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0daeb-105">Para proporcionar a las aplicaciones la máxima flexibilidad en el control de errores, los [servicios de edición de DirectShow](directshow-editing-services.md) usan un mecanismo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0daeb-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="0daeb-106">La aplicación implementa un método para registrar un error.</span><span class="sxs-lookup"><span data-stu-id="0daeb-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="0daeb-107">En tiempo de ejecución, si se produce un error, DES llama al método que ha proporcionado.</span><span class="sxs-lookup"><span data-stu-id="0daeb-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="0daeb-108">El método toma parámetros que describen el error.</span><span class="sxs-lookup"><span data-stu-id="0daeb-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="0daeb-109">Lo que hace el método con esta información depende de usted.</span><span class="sxs-lookup"><span data-stu-id="0daeb-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="0daeb-110">No obstante, debe devolver lo más rápido posible, o podría interferir con la ejecución del programa.</span><span class="sxs-lookup"><span data-stu-id="0daeb-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="0daeb-111">El método de devolución de llamada de registro de errores se encuentra en una interfaz COM, [**IAMErrorLog**](iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="0daeb-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="0daeb-112">La aplicación debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="0daeb-112">Your application must implement this interface.</span></span> <span data-ttu-id="0daeb-113">Al igual que todas las interfaces COM, **IAMErrorLog** hereda la interfaz **IUnknown** , por lo que la aplicación también debe implementarla.</span><span class="sxs-lookup"><span data-stu-id="0daeb-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="0daeb-114">Tiene varias opciones para implementar estas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="0daeb-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="0daeb-115">Puede usar el Active Template Library (ATL), que proporciona implementaciones de existencias de los métodos **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0daeb-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="0daeb-116">DirectShow también proporciona una clase base de C++, [**CUnknown**](cunknown.md), que facilita la implementación de una interfaz com.</span><span class="sxs-lookup"><span data-stu-id="0daeb-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="0daeb-117">Para obtener información sobre el uso de **CUnknown**, vea [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0daeb-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="0daeb-118">En el código de ejemplo de este artículo se define una clase de C++ independiente que implementa **IUnknown** y **IAMErrorLog**.</span><span class="sxs-lookup"><span data-stu-id="0daeb-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="0daeb-119">El resultado no es un objeto COM verdadero, porque no admite **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="0daeb-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="0daeb-120">Sin embargo, este enfoque es adecuado para el propósito del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0daeb-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0daeb-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0daeb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0daeb-122">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="0daeb-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



