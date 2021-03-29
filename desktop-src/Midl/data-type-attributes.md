---
title: Atributos de tipo de datos
description: Puede aplicar estos atributos a los tipos de datos de una instrucción TypeDef para definir más detalladamente el uso o el efecto del tipo de datos.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL, atributos, tipo de datos de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779903"
---
# <a name="data-type-attributes"></a><span data-ttu-id="6caaf-104">Atributos de tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6caaf-104">Data Type Attributes</span></span>

<span data-ttu-id="6caaf-105">Puede aplicar estos atributos a los tipos de datos de una instrucción [**typedef**](typedef.md) para definir más detalladamente el uso o el efecto del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6caaf-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="6caaf-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="6caaf-106">Attribute</span></span>                                 | <span data-ttu-id="6caaf-107">Uso</span><span class="sxs-lookup"><span data-stu-id="6caaf-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6caaf-108">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="6caaf-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="6caaf-109">Identifica un identificador de enlace que mantiene la información de estado (contexto) en un servidor determinado entre las llamadas a procedimientos remotos de un cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="6caaf-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="6caaf-110">No es válido para las funciones de la interfaz de [**objeto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="6caaf-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="6caaf-111">**asa**</span><span class="sxs-lookup"><span data-stu-id="6caaf-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="6caaf-112">Especifica un tipo de identificador personalizado específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6caaf-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="6caaf-113">**Unión de MS \_**</span><span class="sxs-lookup"><span data-stu-id="6caaf-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="6caaf-114">Controla la alineación del NDR de las uniones no encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6caaf-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="6caaf-115">Use en [**typedef**](typedef.md)s para mantener la compatibilidad con las interfaces compiladas con MIDL 1,0 o 2,0.</span><span class="sxs-lookup"><span data-stu-id="6caaf-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="6caaf-116">**codo**</span><span class="sxs-lookup"><span data-stu-id="6caaf-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="6caaf-117">Permite la transmisión de un flujo abierto de datos con tipo a través de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="6caaf-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="6caaf-118">Un parámetro [**in**](in.md) Pipe permite al servidor extraer el flujo de datos del cliente durante una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="6caaf-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="6caaf-119">Un parámetro [**out**](-out.md) Pipe permite que el servidor devuelva la secuencia de datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="6caaf-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="6caaf-120">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="6caaf-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="6caaf-121">Especifica cómo se transmitirá un tipo de datos a través de una red, que se utiliza para la serialización personalizada.</span><span class="sxs-lookup"><span data-stu-id="6caaf-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="6caaf-122">**\_enumeración v1**</span><span class="sxs-lookup"><span data-stu-id="6caaf-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="6caaf-123">Indica que el tipo enumerado especificado se va a transmitir como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6caaf-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="6caaf-124">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="6caaf-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="6caaf-125">Similar a [**transmitir \_ como**](transmit-as.md) , pero se implementan las rutinas para ajustar el tamaño, las referencias, las referencias y la liberación de los datos.</span><span class="sxs-lookup"><span data-stu-id="6caaf-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




