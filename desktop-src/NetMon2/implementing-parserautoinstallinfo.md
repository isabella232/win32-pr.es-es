---
description: Monitor de red usa la función de exportación ParserAutoInstallInfo para instalar un analizador. Cuando se llama a ParserAutoInstallInfo, el analizador devuelve una \_ estructura PF PARSERDLLINFO que contiene toda la información que monitor de red necesita para instalar un archivo dll de analizador.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementación de ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678300"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementación de ParserAutoInstallInfo

Monitor de red usa la función de exportación [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar un analizador. Cuando se llama a **ParserAutoInstallInfo** , el analizador devuelve una estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) que contiene toda la información que monitor de red necesita para instalar un archivo dll de analizador.

> [!Note]  
> Monitor de red mantiene una lista de los analizadores existentes en el archivo [*Parser.ini*](p.md) y crea un archivo ini independiente para cada analizador instalado.

 

Durante el proceso de instalación, el archivo DLL del analizador debe identificar lo siguiente:

-   El número de analizadores en el archivo DLL, incluido el nombre y la descripción del comentario de cada analizador.
-   Los protocolos que preceden al protocolo del analizador.
-   Los protocolos que siguen el protocolo del analizador.

> [!Note]  
> Monitor de red usa la información anterior y siguiente del protocolo del analizador para actualizar los [*conjuntos de entrega*](h.md) y [*seguir los conjuntos*](f.md) de analizadores que identifica el archivo DLL del analizador.

 

En el procedimiento siguiente se identifican los pasos necesarios para implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md).

**Para implementar ParserAutoInstallInfo**

1.  Asigne una estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) mediante **HeapAlloc**.
2.  Devuelva la memoria al montón mediante **HeapFree**.
3.  Tenga en cuenta que esta llamada también debe asignar una estructura [**PF \_ PARSERINFO**](pf-parserinfo.md) para cada analizador del archivo dll.
4.  Especifique el número de analizadores (normalmente uno) que contiene el archivo DLL en el miembro **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Especifique un nombre, un comentario y un archivo de ayuda opcional en los miembros **szProtocolName**, **szComment** y **szHelpFile** de cada estructura [**PF \_ PARSERINFO**](pf-parserinfo.md) .
6.  Especifique los protocolos que preceden a cada protocolo DLL. Una de las condiciones siguientes se aplica a un conjunto de entrega entrante.
    -   Si los protocolos anteriores pueden determinar que el protocolo sigue a partir de los datos de los protocolos anteriores, establezca el miembro **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, el protocolo se agrega a los [*conjuntos de entrega*](h.md) de los protocolos anteriores.
    -   Si los protocolos anteriores no pueden determinar que el protocolo sigue a partir de los datos de los protocolos anteriores, establezca el miembro **pWhoCanPrecedeMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, el protocolo se agrega a continuación a los [*siguientes conjuntos*](f.md) de protocolos.
7.  Especifique los protocolos que siguen a cada protocolo DLL. Una de las condiciones siguientes se aplica a un conjunto de seguimiento de salida.
    -   Si el protocolo puede determinar qué protocolos siguen según los datos del Protocolo, establezca el miembro **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, estos protocolos se agregan al [*conjunto de entrega*](h.md) de los protocolos.
    -   Si el Protocolo no puede determinar qué protocolos siguen según los datos del Protocolo, establezca el miembro **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, estos protocolos se agregan al [*siguiente conjunto*](f.md) del protocolo.
8.  Devuelva la estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) a monitor de red.

La siguiente es una implementación básica de [**ParserAutoInstallInfo**](parserautoinstallinfo.md). El ejemplo de código se toma del analizador genérico que proporciona Monitor de red.

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



