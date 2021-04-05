---
title: Identificadores de enlace
description: El enlace es el proceso de creación de una conexión lógica entre un programa cliente y un programa de servidor. La información que constituye el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533232"
---
# <a name="binding-handles"></a><span data-ttu-id="b64bc-104">Identificadores de enlace</span><span class="sxs-lookup"><span data-stu-id="b64bc-104">Binding Handles</span></span>

<span data-ttu-id="b64bc-105">El enlace es el proceso de creación de una conexión lógica entre un programa cliente y un programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="b64bc-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="b64bc-106">La información que constituye el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="b64bc-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="b64bc-107">Un identificador de enlace es análogo a un identificador de archivo que la función de la biblioteca en tiempo de ejecución fopen de C devuelve, o un identificador de ventana que devuelve la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="b64bc-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="b64bc-108">Al igual que con estos identificadores, la aplicación no puede tener acceso a la información del controlador de enlace ni manipularla directamente.</span><span class="sxs-lookup"><span data-stu-id="b64bc-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="b64bc-109">La información de una estructura de datos de controlador de enlace solo está disponible para las bibliotecas en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="b64bc-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="b64bc-110">Proporciona el identificador, las bibliotecas en tiempo de ejecución tienen acceso y manipulan los datos adecuados.</span><span class="sxs-lookup"><span data-stu-id="b64bc-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="b64bc-111">En esta sección se presenta una descripción de los identificadores de enlace de los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b64bc-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="b64bc-112">Tipos de identificadores de enlace</span><span class="sxs-lookup"><span data-stu-id="b64bc-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="b64bc-113">Enlace del lado cliente</span><span class="sxs-lookup"><span data-stu-id="b64bc-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="b64bc-114">Enlace del lado servidor</span><span class="sxs-lookup"><span data-stu-id="b64bc-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="b64bc-115">Identificadores de enlace completo y parcialmente</span><span class="sxs-lookup"><span data-stu-id="b64bc-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="b64bc-116">Interpretar la información de enlace</span><span class="sxs-lookup"><span data-stu-id="b64bc-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="b64bc-117">Extensiones de Binding-Handle de Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="b64bc-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="b64bc-118">Funciones de control de enlace</span><span class="sxs-lookup"><span data-stu-id="b64bc-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="b64bc-119">La base de datos del servicio de nombres RPC</span><span class="sxs-lookup"><span data-stu-id="b64bc-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 