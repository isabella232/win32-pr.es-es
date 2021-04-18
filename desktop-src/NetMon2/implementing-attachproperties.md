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
# <a name="implementing-attachproperties"></a>Implementación de AttachProperties

Monitor de red llama a la función [**AttachProperties**](attachproperties.md) para asignar las propiedades que existen en un fragmento de datos reconocidos. La función [**AttachProperties**](attachproperties.md) asigna las propiedades a una ubicación específica.

Monitor de red utiliza el siguiente proceso para analizar los datos de un marco.

-   En primer lugar, Monitor de red llama a [RecognizeFrame](recognizeframe.md) para reconocer todos los protocolos que existen en un marco.
-   A continuación, Monitor de red llama a [**AttachProperties**](attachproperties.md) para cada analizador que reconoce un fragmento de datos.

Cuando Monitor de red llama a la función [AttachProperties](attachproperties.md) para los datos reconocidos, el analizador al que se llama debe analizar los datos y, a continuación, asignar cada propiedad existente a una ubicación en los datos reconocidos. El analizador determina qué propiedades existen y dónde se encuentra cada propiedad en los datos. En la ilustración siguiente se muestran datos reconocidos por el analizador.

![datos reconocidos por el analizador](images/attachproperties1.png)

Durante la implementación de [**AttachProperties**](attachproperties.md), debe llamar a una de las siguientes funciones para cada propiedad que exista en una trama de datos.

-   Llame a la función [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) cuando desee modificar los datos de la propiedad en un marco.
-   Llame a la función [**AttachPropertyInstance**](attachpropertyinstance.md) cuando no desee modificar los datos de la propiedad en un marco.

> [!Note]  
> Se recomienda usar los datos tal como existen en la captura.

 

En el procedimiento siguiente se identifican los pasos necesarios para implementar [**AttachProperties**](attachproperties.md).

**Para implementar AttachProperties**

1.  Determine qué propiedades existen y la ubicación de la propiedad en los datos.
2.  Llame a [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) para cada propiedad con un valor que desee modificar.
3.  Llame a [**AttachPropertyInstance**](attachpropertyinstance.md) para cada propiedad con un valor que no desee modificar. Normalmente, esta es la única función a la que debe llamar.

La siguiente es una implementación básica de [**AttachProperties**](attachproperties.md). Tenga en cuenta que en el ejemplo no se incluye el código para determinar qué propiedades existen o el código para buscar las propiedades.

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

 

 



