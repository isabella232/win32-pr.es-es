---
description: Monitor de red utiliza la función de exportación ParserAutoInstallInfo para instalar un analizador. Cuando se llama a ParserAutoInstallInfo, el analizador devuelve una estructura PF PARSERDLLINFO que contiene toda la información que Monitor de red para instalar un \_ archivo DLL del analizador.
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: Implementación de ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743085"
---
# <a name="implementing-parserautoinstallinfo"></a>Implementación de ParserAutoInstallInfo

Monitor de red utiliza la [**función de exportación ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar un analizador. Cuando se llama a **ParserAutoInstallInfo,** el analizador devuelve una estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) que contiene toda la información que Monitor de red para instalar un archivo DLL del analizador.

> [!Note]  
> Monitor de red mantiene una lista de analizadores existentes en el archivo [*Parser.ini*](p.md) y crea un archivo INI independiente para cada analizador instalado.

 

Durante el proceso de instalación, el archivo DLL del analizador debe identificar lo siguiente:

-   Número de analizadores del archivo DLL, incluido un nombre y una descripción de comentario para cada analizador.
-   Protocolos que preceden al protocolo del analizador.
-   Protocolos que siguen al protocolo del analizador.

> [!Note]  
> Monitor de red utiliza la información del protocolo de analizador anterior [](h.md) y siguiente [](f.md) para actualizar los conjuntos de entrega y seguir los conjuntos de analizadores que identifica el archivo DLL del analizador.

 

El procedimiento siguiente identifica los pasos necesarios para implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md).

**Para implementar ParserAutoInstallInfo**

1.  Asigne una [**estructura \_ PF PARSERDLLINFO**](pf-parserdllinfo.md) **mediante HeapAlloc**.
2.  Devuelve memoria al montón mediante **HeapFree.**
3.  Tenga en cuenta que esta llamada también debe asignar una [**estructura PF \_ PARSERINFO**](pf-parserinfo.md) para cada analizador del archivo DLL.
4.  Especifique el número de analizadores (normalmente uno) que contiene el archivo DLL en el **miembro nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).
5.  Especifique un nombre, un comentario y un archivo de Ayuda opcional en los miembros **szProtocolName**, **szComment** y **szHelpFile** de cada [**estructura PF \_ PARSERINFO.**](pf-parserinfo.md)
6.  Especifique los protocolos que preceden a cada protocolo DLL. Una de las siguientes condiciones se aplica a un conjunto de entregas entrantes.
    -   Si los protocolos anteriores pueden determinar que el protocolo sigue a los datos de los protocolos anteriores, establezca el miembro **pHandHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, el protocolo se agrega a los conjuntos [*de entrega*](h.md) de los protocolos anteriores.
    -   Si los protocolos anteriores no pueden determinar que el protocolo sigue a los datos de los protocolos anteriores, establezca el miembro **pWhoCanPrecedeMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, el protocolo se agrega a los [*siguientes conjuntos*](f.md) de protocolos.
7.  Especifique los protocolos que siguen a cada protocolo DLL. Una de las siguientes condiciones se aplica a un conjunto de seguimiento saliente.
    -   Si el protocolo puede determinar qué protocolos siguen en función de los datos del protocolo, establezca el **miembro pHandDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, estos protocolos se agregan al [*conjunto de entrega*](h.md) de los protocolos.
    -   Si el protocolo no puede determinar qué protocolos se siguen en función de los datos del protocolo, establezca el **miembro pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md). En este caso, estos protocolos se agregan al [*siguiente conjunto*](f.md) de protocolos.
8.  Devuelve la [**estructura \_ PF PARSERDLLINFO**](pf-parserdllinfo.md) a Monitor de red.

A continuación se muestra una implementación básica [**de ParserAutoInstallInfo**](parserautoinstallinfo.md). El ejemplo de código se toma del analizador genérico que Monitor de red proporciona.

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

 

 



