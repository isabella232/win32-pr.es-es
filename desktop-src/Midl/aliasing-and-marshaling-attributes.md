---
title: Atributos de alias y serialización
description: Las aplicaciones distribuidas casi siempre pasan datos entre los programas de cliente y servidor cuando llaman a procedimientos de interfaz.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- MIDL de IDL, atributos MIDL, alias y serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076303"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="360b4-104">Atributos de alias y serialización</span><span class="sxs-lookup"><span data-stu-id="360b4-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="360b4-105">Las aplicaciones distribuidas casi siempre pasan datos entre los programas de cliente y servidor cuando llaman a procedimientos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="360b4-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="360b4-106">Los programadores utilizan MIDL para describir los datos que los programas de cliente y servidor pasan de forma estándar.</span><span class="sxs-lookup"><span data-stu-id="360b4-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="360b4-107">El compilador MIDL crea programas de código auxiliar de aplicación, o proxy, para el cliente y el servidor que convierte los datos en un formato normalizado que se puede enviar a través de una red.</span><span class="sxs-lookup"><span data-stu-id="360b4-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="360b4-108">Este formato, el formato de representación de datos de red (NDR), a menudo se denomina formato de conexión de los datos.</span><span class="sxs-lookup"><span data-stu-id="360b4-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="360b4-109">El código auxiliar debe convertir los datos de su formato nativo en el espacio de memoria del programa a NDR.</span><span class="sxs-lookup"><span data-stu-id="360b4-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="360b4-110">Esta conversión se denomina cálculo de referencias de los datos.</span><span class="sxs-lookup"><span data-stu-id="360b4-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="360b4-111">Cuando un cliente o un programa de servidor recibe datos, debe convertir los datos de NDR al formato nativo para ese programa.</span><span class="sxs-lookup"><span data-stu-id="360b4-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="360b4-112">Esto se denomina anulación del cálculo de referencias de los datos.</span><span class="sxs-lookup"><span data-stu-id="360b4-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="360b4-113">Use atributos de alias y serialización para controlar el modo en que los datos se empaquetan en formato NDR y se transmiten a través de la red.</span><span class="sxs-lookup"><span data-stu-id="360b4-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="360b4-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="360b4-114">Attribute</span></span>                             | <span data-ttu-id="360b4-115">Uso</span><span class="sxs-lookup"><span data-stu-id="360b4-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="360b4-116">**llamar a \_ como**</span><span class="sxs-lookup"><span data-stu-id="360b4-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="360b4-117">Asigna una función no utilizables a una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="360b4-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="360b4-118">**IID \_ es**</span><span class="sxs-lookup"><span data-stu-id="360b4-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="360b4-119">Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.</span><span class="sxs-lookup"><span data-stu-id="360b4-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="360b4-120">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="360b4-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="360b4-121">Convierte un tipo de datos en un tipo más simple para su transmisión a través de una red.</span><span class="sxs-lookup"><span data-stu-id="360b4-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="360b4-122">**\_serialización de cable**</span><span class="sxs-lookup"><span data-stu-id="360b4-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="360b4-123">Similar a [**transmitir \_ como**](transmit-as.md) , pero se implementan las rutinas para ajustar el tamaño, las referencias, las referencias y la liberación de los datos.</span><span class="sxs-lookup"><span data-stu-id="360b4-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="360b4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="360b4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360b4-125">Atributos ACF de conversión y serialización de tipos</span><span class="sxs-lookup"><span data-stu-id="360b4-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




