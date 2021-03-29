---
description: Los controladores de excepciones de vectores son una extensión del control estructurado de excepciones.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Control de excepciones vectoriales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907229"
---
# <a name="vectored-exception-handling"></a><span data-ttu-id="b74d3-103">Control de excepciones vectoriales</span><span class="sxs-lookup"><span data-stu-id="b74d3-103">Vectored Exception Handling</span></span>

<span data-ttu-id="b74d3-104">Los controladores de excepciones de vectores son una extensión del control estructurado de excepciones.</span><span class="sxs-lookup"><span data-stu-id="b74d3-104">Vectored exception handlers are an extension to structured exception handling.</span></span> <span data-ttu-id="b74d3-105">Una aplicación puede registrar una función para ver o controlar todas las excepciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b74d3-105">An application can register a function to watch or handle all exceptions for the application.</span></span> <span data-ttu-id="b74d3-106">Los controladores vectoriales no están basados en marcos; por lo tanto, puede Agregar un controlador que se llamará independientemente de dónde se encuentre en un marco de llamada.</span><span class="sxs-lookup"><span data-stu-id="b74d3-106">Vectored handlers are not frame-based, therefore, you can add a handler that will be called regardless of where you are in a call frame.</span></span> <span data-ttu-id="b74d3-107">Se llama a los controladores vectoriales en el orden en que se agregaron, después de que el depurador obtenga una notificación de primera oportunidad, pero antes de que el sistema comience a desenredar la pila.</span><span class="sxs-lookup"><span data-stu-id="b74d3-107">Vectored handlers are called in the order that they were added, after the debugger gets a first chance notification, but before the system begins unwinding the stack.</span></span>

<span data-ttu-id="b74d3-108">Para agregar un controlador de continuación de vectores, utilice la función [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="b74d3-108">To add a vectored continue handler, use the [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) function.</span></span> <span data-ttu-id="b74d3-109">Para quitar este controlador, utilice la función [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .</span><span class="sxs-lookup"><span data-stu-id="b74d3-109">To remove this handler, use the [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) function.</span></span>

<span data-ttu-id="b74d3-110">Para agregar un controlador de excepciones vectoriales, utilice la función [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="b74d3-110">To add a vectored exception handler, use the [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) function.</span></span> <span data-ttu-id="b74d3-111">Para quitar este controlador, utilice la función [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .</span><span class="sxs-lookup"><span data-stu-id="b74d3-111">To remove this handler, use the [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) function.</span></span>

 

 
