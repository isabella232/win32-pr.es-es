---
title: Type-Conversion y serialización de atributos ACF
description: Utilice estos atributos para controlar cómo se transmiten los datos a través de la red.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- Los MIDL, atributos, conversión de tipos y serialización de tipo ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994475"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="c0c4a-104">Type-Conversion y serialización de atributos ACF</span><span class="sxs-lookup"><span data-stu-id="c0c4a-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="c0c4a-105">Utilice estos atributos para controlar cómo se transmiten los datos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="c0c4a-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="c0c4a-106">Attribute</span></span>                                        | <span data-ttu-id="c0c4a-107">Uso</span><span class="sxs-lookup"><span data-stu-id="c0c4a-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c4a-108">descodificación de [**codificación**](encode.md)[](decode.md)</span><span class="sxs-lookup"><span data-stu-id="c0c4a-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="c0c4a-109">Indica a MIDL que exponga las rutinas de serialización de tipo o procedimiento (picking) que genera para el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="c0c4a-110">La aplicación cliente puede llamar a esas rutinas para calcular las referencias de datos por valor.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="c0c4a-111">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="c0c4a-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="c0c4a-112">Especifica cómo se representará un tipo de datos en la conexión, cuando la naturaleza exacta del tipo de datos de un cliente no es importante para el servidor (porque solo necesita los datos en sí y no la estructura real), o bien el tipo de cliente real es desconocido para MIDL en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="c0c4a-113">Por ejemplo, si la aplicación cliente usa una lista vinculada de números de punto flotante, podría especificar que la representación por cable de esa lista sea una matriz de tipo [**float**](float.md).</span><span class="sxs-lookup"><span data-stu-id="c0c4a-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="c0c4a-114">**\_serialización de usuario**</span><span class="sxs-lookup"><span data-stu-id="c0c4a-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="c0c4a-115">Controla cómo se transmiten los datos a través de la conexión implementando sus propias rutinas de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="c0c4a-116">Este atributo es útil si tiene un tipo de datos desconocido para MIDL o si va a pasar información entre plataformas big-endian y Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="c0c4a-117">Los atributos de serialización [**de DCE en \_ línea**](in-line.md) y [**fuera \_ de \_ línea**](out-of-line.md) no se implementan en Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="c0c4a-118">El compilador MIDL calcula automáticamente las referencias de tipos de datos complejos fuera de línea.</span><span class="sxs-lookup"><span data-stu-id="c0c4a-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




