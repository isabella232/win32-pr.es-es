---
title: Interfaces en objetos distribuidos
description: En el computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperen entre distintos contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfaces MIDL, en objetos distribuidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358926"
---
# <a name="interfaces-in-distributed-objects"></a><span data-ttu-id="a21fd-104">Interfaces en objetos distribuidos</span><span class="sxs-lookup"><span data-stu-id="a21fd-104">Interfaces in Distributed Objects</span></span>

<span data-ttu-id="a21fd-105">En el computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperen entre distintos contextos.</span><span class="sxs-lookup"><span data-stu-id="a21fd-105">In distributed computing, an interface is a collection of definitions and remote functions that enables two or more programs to interoperate between different contexts.</span></span> <span data-ttu-id="a21fd-106">En una aplicación RPC, una interfaz especifica:</span><span class="sxs-lookup"><span data-stu-id="a21fd-106">In an RPC application, an interface specifies:</span></span>

-   <span data-ttu-id="a21fd-107">Cómo se identifican entre sí las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="a21fd-107">How client and server applications identify themselves to each other.</span></span>
-   <span data-ttu-id="a21fd-108">Cómo se transmiten los datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="a21fd-108">How data is transmitted between client and server.</span></span>
-   <span data-ttu-id="a21fd-109">Procedimientos remotos a los que puede llamar la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a21fd-109">Remote procedures that the client application can call.</span></span>
-   <span data-ttu-id="a21fd-110">Tipos de datos para los parámetros y valores devueltos de los procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="a21fd-110">Data types for the parameters and return values of the remote procedures.</span></span>

<span data-ttu-id="a21fd-111">El Lenguaje de definición de interfaz de Microsoft (MIDL) es para implementar interfaces utilizadas en aplicaciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="a21fd-111">The Microsoft Interface Definition Language (MIDL) is for implementing interfaces used in distributed applications.</span></span> <span data-ttu-id="a21fd-112">Con MIDL, una aplicación puede tener una interfaz o varias.</span><span class="sxs-lookup"><span data-stu-id="a21fd-112">With MIDL, an application can have one interface or many.</span></span> <span data-ttu-id="a21fd-113">Cada interfaz especifica un contrato distribuido único entre los programas de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="a21fd-113">Each interface specifies a unique distributed contract between the client and server programs.</span></span> <span data-ttu-id="a21fd-114">Las aplicaciones basadas en llamadas a procedimiento remoto (RPC), el modelo de objetos componentes (COM) y el modelo de objetos componentes distribuido (DCOM) especifican sus interfaces mediante MIDL.</span><span class="sxs-lookup"><span data-stu-id="a21fd-114">Applications based on remote procedure calls (RPC), Component Object Model (COM), and Distributed Component Object Model (DCOM) specify their interfaces using MIDL.</span></span>

<span data-ttu-id="a21fd-115">MIDL es similar a C y C++ en muchos sentidos.</span><span class="sxs-lookup"><span data-stu-id="a21fd-115">MIDL resembles C and C++ in many ways.</span></span> <span data-ttu-id="a21fd-116">Para obtener información general sobre la escritura de interfaces MIDL, vea [desarrollar la interfaz](/windows/desktop/Rpc/developing-the-interface).</span><span class="sxs-lookup"><span data-stu-id="a21fd-116">For an overview of writing MIDL interfaces, see [Developing the Interface](/windows/desktop/Rpc/developing-the-interface).</span></span>

 

 