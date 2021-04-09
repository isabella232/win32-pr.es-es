---
title: Atributos ACF de enlace
description: Especifique cómo el cliente se conecta al servidor para las llamadas a procedimientos remotos con los atributos que se muestran en la tabla siguiente.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF (MIDL), atributos, enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076120"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="19f32-104">Atributos ACF de enlace</span><span class="sxs-lookup"><span data-stu-id="19f32-104">Binding ACF Attributes</span></span>

<span data-ttu-id="19f32-105">Especifique cómo el cliente se conecta al servidor para las llamadas a procedimientos remotos con los atributos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="19f32-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="19f32-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="19f32-106">Attribute</span></span>                                                          | <span data-ttu-id="19f32-107">Uso</span><span class="sxs-lookup"><span data-stu-id="19f32-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19f32-108">**async**</span><span class="sxs-lookup"><span data-stu-id="19f32-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="19f32-109">Define un identificador que permite al llamador realizar una llamada asincrónica y devolver inmediatamente sin esperar los resultados y, a continuación, volver a sincronizar con la función llamada para recibir los datos después de que se complete la llamada.</span><span class="sxs-lookup"><span data-stu-id="19f32-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="19f32-110">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="19f32-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="19f32-111">Indica a MIDL que permita que el código auxiliar Controle automáticamente el enlace.</span><span class="sxs-lookup"><span data-stu-id="19f32-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="19f32-112">Este es el valor predeterminado si no se especifica ningún controlador de enlace.</span><span class="sxs-lookup"><span data-stu-id="19f32-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="19f32-113">**identificador de contexto de \_ \_ noserialización**</span><span class="sxs-lookup"><span data-stu-id="19f32-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="19f32-114">Garantiza que nunca se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19f32-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="19f32-115">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="19f32-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="19f32-116">Garantiza que siempre se serializará un identificador de contexto, independientemente del comportamiento predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="19f32-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="19f32-117">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="19f32-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="19f32-118">Permite que la aplicación cliente controle el enlace con un parámetro explícito en cada procedimiento.</span><span class="sxs-lookup"><span data-stu-id="19f32-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="19f32-119">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="19f32-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="19f32-120">Especifica un identificador para los procedimientos que no tienen un parámetro de identificador explícito.</span><span class="sxs-lookup"><span data-stu-id="19f32-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="19f32-121">La aplicación cliente sigue controlando el enlace.</span><span class="sxs-lookup"><span data-stu-id="19f32-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="19f32-122">**\_identificador de contexto estricto \_**</span><span class="sxs-lookup"><span data-stu-id="19f32-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="19f32-123">Garantiza que los métodos de la interfaz solo aceptarán los identificadores de contexto creados por un método de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="19f32-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




