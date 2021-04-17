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
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="75963-104">Implementación de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="75963-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="75963-105">Monitor de red usa la función de exportación [**ParserAutoInstallInfo**](parserautoinstallinfo.md) para instalar un analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="75963-106">Cuando se llama a **ParserAutoInstallInfo** , el analizador devuelve una estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) que contiene toda la información que monitor de red necesita para instalar un archivo dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="75963-107">Monitor de red mantiene una lista de los analizadores existentes en el archivo [*Parser.ini*](p.md) y crea un archivo ini independiente para cada analizador instalado.</span><span class="sxs-lookup"><span data-stu-id="75963-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="75963-108">Durante el proceso de instalación, el archivo DLL del analizador debe identificar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="75963-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="75963-109">El número de analizadores en el archivo DLL, incluido el nombre y la descripción del comentario de cada analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="75963-110">Los protocolos que preceden al protocolo del analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="75963-111">Los protocolos que siguen el protocolo del analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="75963-112">Monitor de red usa la información anterior y siguiente del protocolo del analizador para actualizar los [*conjuntos de entrega*](h.md) y [*seguir los conjuntos*](f.md) de analizadores que identifica el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="75963-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="75963-113">En el procedimiento siguiente se identifican los pasos necesarios para implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="75963-114">**Para implementar ParserAutoInstallInfo**</span><span class="sxs-lookup"><span data-stu-id="75963-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="75963-115">Asigne una estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) mediante **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="75963-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="75963-116">Devuelva la memoria al montón mediante **HeapFree**.</span><span class="sxs-lookup"><span data-stu-id="75963-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="75963-117">Tenga en cuenta que esta llamada también debe asignar una estructura [**PF \_ PARSERINFO**](pf-parserinfo.md) para cada analizador del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="75963-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="75963-118">Especifique el número de analizadores (normalmente uno) que contiene el archivo DLL en el miembro **nParsers** de [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="75963-119">Especifique un nombre, un comentario y un archivo de ayuda opcional en los miembros **szProtocolName**, **szComment** y **szHelpFile** de cada estructura [**PF \_ PARSERINFO**](pf-parserinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="75963-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="75963-120">Especifique los protocolos que preceden a cada protocolo DLL.</span><span class="sxs-lookup"><span data-stu-id="75963-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="75963-121">Una de las condiciones siguientes se aplica a un conjunto de entrega entrante.</span><span class="sxs-lookup"><span data-stu-id="75963-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="75963-122">Si los protocolos anteriores pueden determinar que el protocolo sigue a partir de los datos de los protocolos anteriores, establezca el miembro **pWhoHandsOffToMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="75963-123">En este caso, el protocolo se agrega a los [*conjuntos de entrega*](h.md) de los protocolos anteriores.</span><span class="sxs-lookup"><span data-stu-id="75963-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="75963-124">Si los protocolos anteriores no pueden determinar que el protocolo sigue a partir de los datos de los protocolos anteriores, establezca el miembro **pWhoCanPrecedeMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="75963-125">En este caso, el protocolo se agrega a continuación a los [*siguientes conjuntos*](f.md) de protocolos.</span><span class="sxs-lookup"><span data-stu-id="75963-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="75963-126">Especifique los protocolos que siguen a cada protocolo DLL.</span><span class="sxs-lookup"><span data-stu-id="75963-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="75963-127">Una de las condiciones siguientes se aplica a un conjunto de seguimiento de salida.</span><span class="sxs-lookup"><span data-stu-id="75963-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="75963-128">Si el protocolo puede determinar qué protocolos siguen según los datos del Protocolo, establezca el miembro **pWhoDoIHandOffTo** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="75963-129">En este caso, estos protocolos se agregan al [*conjunto de entrega*](h.md) de los protocolos.</span><span class="sxs-lookup"><span data-stu-id="75963-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="75963-130">Si el Protocolo no puede determinar qué protocolos siguen según los datos del Protocolo, establezca el miembro **pWhoCanFollowMe** de [**PF \_ PARSERINFO**](pf-parserinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="75963-131">En este caso, estos protocolos se agregan al [*siguiente conjunto*](f.md) del protocolo.</span><span class="sxs-lookup"><span data-stu-id="75963-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="75963-132">Devuelva la estructura [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) a monitor de red.</span><span class="sxs-lookup"><span data-stu-id="75963-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="75963-133">La siguiente es una implementación básica de [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span><span class="sxs-lookup"><span data-stu-id="75963-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="75963-134">El ejemplo de código se toma del analizador genérico que proporciona Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="75963-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

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

 

 



