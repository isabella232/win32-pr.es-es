---
description: Llama a la función AttachProperties para asignar las propiedades que existen en un fragmento de datos reconocidos.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementación de AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677517"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="13db4-103">Implementación de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="13db4-103">Implementing AttachProperties</span></span>

<span data-ttu-id="13db4-104">Monitor de red llama a la función [**AttachProperties**](attachproperties.md) para asignar las propiedades que existen en un fragmento de datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="13db4-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="13db4-105">La función [**AttachProperties**](attachproperties.md) asigna las propiedades a una ubicación específica.</span><span class="sxs-lookup"><span data-stu-id="13db4-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="13db4-106">Monitor de red utiliza el siguiente proceso para analizar los datos de un marco.</span><span class="sxs-lookup"><span data-stu-id="13db4-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="13db4-107">En primer lugar, Monitor de red llama a [RecognizeFrame](recognizeframe.md) para reconocer todos los protocolos que existen en un marco.</span><span class="sxs-lookup"><span data-stu-id="13db4-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="13db4-108">A continuación, Monitor de red llama a [**AttachProperties**](attachproperties.md) para cada analizador que reconoce un fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="13db4-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="13db4-109">Cuando Monitor de red llama a la función [AttachProperties](attachproperties.md) para los datos reconocidos, el analizador al que se llama debe analizar los datos y, a continuación, asignar cada propiedad existente a una ubicación en los datos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="13db4-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="13db4-110">El analizador determina qué propiedades existen y dónde se encuentra cada propiedad en los datos.</span><span class="sxs-lookup"><span data-stu-id="13db4-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="13db4-111">En la ilustración siguiente se muestran datos reconocidos por el analizador.</span><span class="sxs-lookup"><span data-stu-id="13db4-111">The following figure shows parser-recognized data.</span></span>

![datos reconocidos por el analizador](images/attachproperties1.png)

<span data-ttu-id="13db4-113">Durante la implementación de [**AttachProperties**](attachproperties.md), debe llamar a una de las siguientes funciones para cada propiedad que exista en una trama de datos.</span><span class="sxs-lookup"><span data-stu-id="13db4-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="13db4-114">Llame a la función [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) cuando desee modificar los datos de la propiedad en un marco.</span><span class="sxs-lookup"><span data-stu-id="13db4-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="13db4-115">Llame a la función [**AttachPropertyInstance**](attachpropertyinstance.md) cuando no desee modificar los datos de la propiedad en un marco.</span><span class="sxs-lookup"><span data-stu-id="13db4-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="13db4-116">Se recomienda usar los datos tal como existen en la captura.</span><span class="sxs-lookup"><span data-stu-id="13db4-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="13db4-117">En el procedimiento siguiente se identifican los pasos necesarios para implementar [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="13db4-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="13db4-118">**Para implementar AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="13db4-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="13db4-119">Determine qué propiedades existen y la ubicación de la propiedad en los datos.</span><span class="sxs-lookup"><span data-stu-id="13db4-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="13db4-120">Llame a [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para cada propiedad con un valor que desee modificar.</span><span class="sxs-lookup"><span data-stu-id="13db4-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="13db4-121">Llame a [**AttachPropertyInstance**](attachpropertyinstance.md) para cada propiedad con un valor que no desee modificar.</span><span class="sxs-lookup"><span data-stu-id="13db4-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="13db4-122">Normalmente, esta es la única función a la que debe llamar.</span><span class="sxs-lookup"><span data-stu-id="13db4-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="13db4-123">La siguiente es una implementación básica de [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="13db4-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="13db4-124">Tenga en cuenta que en el ejemplo no se incluye el código para determinar qué propiedades existen o el código para buscar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="13db4-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



