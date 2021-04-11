---
description: Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Crear clases de Windows en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910641"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="91376-103">Crear clases de Windows en paralelo</span><span class="sxs-lookup"><span data-stu-id="91376-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="91376-104">Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo.</span><span class="sxs-lookup"><span data-stu-id="91376-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="91376-105">Mediante el uso de clases de Windows en paralelo, la aplicación puede tener versiones diferentes de una clase activa al mismo tiempo en una ventana primaria única.</span><span class="sxs-lookup"><span data-stu-id="91376-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="91376-106">Para crear una clase de Windows en paralelo, la aplicación debe activar un contexto de activación antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obtener un identificador de la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="91376-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="91376-107">Por ejemplo, los controles comunes de Windows versión 5,82 y versión 6,0 tienen un control de edición.</span><span class="sxs-lookup"><span data-stu-id="91376-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="91376-108">De forma predeterminada, Windows usa el control de edición de la versión 5,82.</span><span class="sxs-lookup"><span data-stu-id="91376-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="91376-109">Para obtener una ventana en paralelo que tenga el control de edición de la versión 6,0, antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costumbre, la aplicación puede hacer referencia a un ensamblado que exponga clases de ventana con nombre y, a continuación, activar el contexto de activación que hace referencia a los controles de la versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="91376-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
