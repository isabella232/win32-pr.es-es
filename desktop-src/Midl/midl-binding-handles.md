---
title: Identificadores de enlace MIDL
description: Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipos de datos MIDL, identificadores de enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077584"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="6214d-104">Identificadores de enlace MIDL</span><span class="sxs-lookup"><span data-stu-id="6214d-104">MIDL Binding Handles</span></span>

<span data-ttu-id="6214d-105">Los identificadores de enlace son objetos de datos que representan el enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6214d-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="6214d-106">MIDL admite el identificador de tipo base [**\_ t**](handle-t.md).</span><span class="sxs-lookup"><span data-stu-id="6214d-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="6214d-107">Los identificadores de este tipo se conocen como "identificadores primitivos".</span><span class="sxs-lookup"><span data-stu-id="6214d-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="6214d-108">Puede definir sus propios tipos de identificador mediante el atributo **\[ Handle \]** .</span><span class="sxs-lookup"><span data-stu-id="6214d-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="6214d-109">Los identificadores definidos de esta manera se conocen como identificadores "definidos por el usuario" o "personalizados" o "genéricos".</span><span class="sxs-lookup"><span data-stu-id="6214d-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="6214d-110">También puede definir un identificador que mantenga la información de estado mediante el atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6214d-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="6214d-111">Los identificadores definidos de esta manera se conocen como identificadores de "contexto".</span><span class="sxs-lookup"><span data-stu-id="6214d-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="6214d-112">Si no se necesita información de estado y no elige llamar a las bibliotecas en tiempo de ejecución de RPC para administrar el identificador, puede solicitar que las bibliotecas en tiempo de ejecución proporcionen enlaces automáticos.</span><span class="sxs-lookup"><span data-stu-id="6214d-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="6214d-113">Esto se hace mediante la palabra clave ACF de **\[** [**\_ identificador automático**](auto-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="6214d-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="6214d-114">Puede especificar una variable global como identificador de enlace mediante el uso del **\[** [**\_ identificador implícito**](implicit-handle.md)de la palabra clave ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="6214d-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="6214d-115">La palabra clave de **\[ \_ identificador \] explícito** se usa para indicar que cada función remota tiene un identificador especificado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="6214d-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="6214d-116">Para obtener más información, vea [enlazar y controlar](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="6214d-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 