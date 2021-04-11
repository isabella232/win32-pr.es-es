---
description: Monitores de red llama a la función RecognizeFrame de un analizador para determinar que el analizador reconoce los datos no reclamados de un marco.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementación de RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361388"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="d4e60-103">Implementación de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="d4e60-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="d4e60-104">Monitores de red llama a la función [**RecognizeFrame**](recognizeframe.md) de un analizador para determinar que el analizador reconoce los datos no reclamados de un marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="d4e60-105">Los datos no reclamados pueden estar al principio de un fotograma, pero normalmente los datos no reclamados se encuentran en medio de un marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="d4e60-106">En la ilustración siguiente se muestran datos no reclamados ubicados en medio de un marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![datos no reclamados ubicados en medio de un marco](images/recognizeframe1.png)

<span data-ttu-id="d4e60-108">Monitor de red proporciona la siguiente información cuando llama a la función [**RecognizeFrame**](recognizeframe.md) :</span><span class="sxs-lookup"><span data-stu-id="d4e60-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="d4e60-109">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-109">A handle to the frame.</span></span>
-   <span data-ttu-id="d4e60-110">Puntero al principio del marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="d4e60-111">Puntero al inicio de los datos no reclamados.</span><span class="sxs-lookup"><span data-stu-id="d4e60-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="d4e60-112">Valor MAC del primer protocolo del marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="d4e60-113">El número de bytes de los datos no reclamados; es decir, los bytes restantes en el marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="d4e60-114">Identificador del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="d4e60-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="d4e60-115">Desplazamiento del protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="d4e60-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="d4e60-116">Cuando el archivo DLL del analizador determina que los datos no reclamados se inician con el protocolo del analizador, el archivo DLL del analizador determina dónde comienza el siguiente protocolo y qué protocolo sigue.</span><span class="sxs-lookup"><span data-stu-id="d4e60-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="d4e60-117">La DLL del analizador funciona de las siguientes maneras condicionales:</span><span class="sxs-lookup"><span data-stu-id="d4e60-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="d4e60-118">Si el archivo DLL del analizador reconoce datos no reclamados, el archivo DLL del analizador establece el parámetro *pProtocolStatus* y devuelve un puntero al siguiente protocolo en el marco o **null**.</span><span class="sxs-lookup"><span data-stu-id="d4e60-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="d4e60-119">Se devuelve **null** si el protocolo actual es el último protocolo del marco.</span><span class="sxs-lookup"><span data-stu-id="d4e60-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="d4e60-120">Si el archivo DLL del analizador reconoce datos no reclamados e identifica el protocolo que sigue (a partir de la información proporcionada en el protocolo), el archivo DLL del analizador devuelve un puntero al identificador del protocolo siguiente en el parámetro *phNextProtocol* de la función.</span><span class="sxs-lookup"><span data-stu-id="d4e60-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="d4e60-121">Si el archivo DLL del analizador no reconoce los datos no reclamados, el archivo DLL del analizador devuelve el puntero al inicio de los datos no reclamados y Monitor de red continúa intentando analizar los datos no reclamados.</span><span class="sxs-lookup"><span data-stu-id="d4e60-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="d4e60-122">**Para implementar RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="d4e60-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="d4e60-123">Pruebe para determinar que reconoce el protocolo.</span><span class="sxs-lookup"><span data-stu-id="d4e60-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="d4e60-124">Si reconoce datos no reclamados y sabe qué protocolo sigue, establezca *pProtocolStatus* en protocolo \_ \_ siguiente \_ Protocolo, establezca *phNextProtocol* en un puntero que apunte al identificador del siguiente protocolo y, a continuación, devuelva un puntero al protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4e60-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="d4e60-125">-o bien-</span><span class="sxs-lookup"><span data-stu-id="d4e60-125">–or–</span></span>

    <span data-ttu-id="d4e60-126">Si reconoce datos no reclamados y no sabe qué protocolo sigue, establezca *pProtocolStatus* en estado de protocolo \_ \_ reconocido y, a continuación, devuelva un puntero al protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4e60-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="d4e60-127">-o bien-</span><span class="sxs-lookup"><span data-stu-id="d4e60-127">–or–</span></span>

    <span data-ttu-id="d4e60-128">Si reconoce datos no reclamados y el protocolo es el último protocolo de un marco, establezca *pProtocolStatus* en estado de \_ Protocolo \_ reclamado y, a continuación, devuelva **null**.</span><span class="sxs-lookup"><span data-stu-id="d4e60-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="d4e60-129">-o bien-</span><span class="sxs-lookup"><span data-stu-id="d4e60-129">–or–</span></span>

    <span data-ttu-id="d4e60-130">Si no reconoce los datos no notificados, establezca *pProtocolStatus* en estado de \_ Protocolo \_ no \_ reconocido y, a continuación, devuelva el puntero que se le pasa en *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="d4e60-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="d4e60-131">La siguiente es una implementación básica de [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="d4e60-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



