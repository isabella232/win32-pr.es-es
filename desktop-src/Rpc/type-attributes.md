---
title: Atributos de tipo
description: La llamada a procedimiento remoto (RPC) y los atributos de tipo MIDL que se pueden aplicar a las declaraciones de tipos.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904618"
---
# <a name="type-attributes"></a><span data-ttu-id="f515e-103">Atributos de tipo</span><span class="sxs-lookup"><span data-stu-id="f515e-103">Type Attributes</span></span>

<span data-ttu-id="f515e-104">Los atributos de tipo son los atributos MIDL que se pueden aplicar a las declaraciones de tipos:</span><span class="sxs-lookup"><span data-stu-id="f515e-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="f515e-105">**\[**[**asa**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="f515e-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="f515e-106">**\[**[**identificador de contexto \_**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="f515e-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="f515e-107">**\[**[**tipo de conmutador \_**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="f515e-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="f515e-108">atributos de tipo de puntero</span><span class="sxs-lookup"><span data-stu-id="f515e-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="f515e-109">El atributo de **\[ \_ tipo \] de conmutador** designa el tipo de un discriminador de Unión.</span><span class="sxs-lookup"><span data-stu-id="f515e-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="f515e-110">Este atributo solo se aplica a una Unión no encapsulada.</span><span class="sxs-lookup"><span data-stu-id="f515e-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="f515e-111">Un identificador de contexto es un puntero con un atributo de **\[ \_ identificador \] de contexto** .</span><span class="sxs-lookup"><span data-stu-id="f515e-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="f515e-112">El atributo de **\[ \_ identificador \] de contexto** permite escribir procedimientos que mantienen información de estado entre llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="f515e-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="f515e-113">Un identificador de contexto con un valor distinto de NULL representa el contexto guardado y sirve para dos propósitos:</span><span class="sxs-lookup"><span data-stu-id="f515e-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="f515e-114">En el lado del cliente, contiene la información necesaria para que la biblioteca en tiempo de ejecución de RPC dirija la llamada al servidor.</span><span class="sxs-lookup"><span data-stu-id="f515e-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="f515e-115">En el lado del servidor, actúa como un identificador en el contexto activo.</span><span class="sxs-lookup"><span data-stu-id="f515e-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="f515e-116">El **\[** [](/windows/desktop/Midl/handle) **\]** atributo Handle especifica que un tipo puede aparecer como un identificador definido por el usuario (Genérico).</span><span class="sxs-lookup"><span data-stu-id="f515e-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="f515e-117">Esta característica permite el diseño de identificadores que son significativos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f515e-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="f515e-118">El usuario debe proporcionar rutinas de enlace y desenlace para realizar la conversión entre el tipo de identificador definido por el usuario y el tipo de identificador primitivo de RPC, **Handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="f515e-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="f515e-119">Un identificador primitivo contiene información de destino significativa para las bibliotecas en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="f515e-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="f515e-120">Un identificador definido por el usuario solo se puede definir en una declaración de tipos, no en una declaración de función.</span><span class="sxs-lookup"><span data-stu-id="f515e-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="f515e-121">Un parámetro con el atributo **\[ Handle \]** tiene un doble propósito.</span><span class="sxs-lookup"><span data-stu-id="f515e-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="f515e-122">Se utiliza para determinar el enlace de la llamada y se transmite al procedimiento llamado como un parámetro de datos normal.</span><span class="sxs-lookup"><span data-stu-id="f515e-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 