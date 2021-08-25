---
description: Monitores de red llama a la función RecognizeFrame de un analizador para determinar que el analizador reconoce los datos no reclamados de un fotograma.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementación de RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890505"
---
# <a name="implementing-recognizeframe"></a>Implementación de RecognizeFrame

Monitores de red llama a la función [**RecognizeFrame**](recognizeframe.md) de un analizador para determinar que el analizador reconoce los datos no reclamados de un fotograma. Los datos no reclamados pueden estar al principio de un fotograma, pero normalmente, los datos no reclamados se encuentran en medio de un marco. En la ilustración siguiente se muestran los datos no reclamados ubicados en medio de un marco.

![datos no reclamados ubicados en medio de un marco](images/recognizeframe1.png)

Monitor de red proporciona la siguiente información cuando llama a la [**función RecognizeFrame:**](recognizeframe.md)

-   Identificador del marco.
-   Puntero al inicio del marco.
-   Puntero al inicio de los datos no reclamados.
-   Valor mac del primer protocolo del marco.
-   Número de bytes de los datos no reclamados; es decir, los bytes restantes en el marco.
-   Identificador del protocolo anterior.
-   Desplazamiento del protocolo anterior.

Cuando el archivo DLL del analizador determina que los datos no reclamados comienzan por el protocolo del analizador, el archivo DLL del analizador determina dónde se inicia el siguiente protocolo y qué protocolo sigue. La DLL del analizador funciona de las siguientes maneras condicionales:

-   Si el archivo DLL del analizador reconoce datos no reclamados, el archivo DLL del analizador establece el parámetro *pProtocolStatus* y devuelve un puntero al siguiente protocolo del marco o **NULL.** **Se** devuelve NULL si el protocolo actual es el último protocolo del marco.
-   Si el archivo DLL del analizador reconoce los datos no reclamados e identifica el protocolo que sigue (a partir de la información proporcionada en el protocolo), el archivo DLL del analizador devuelve un puntero al identificador del protocolo siguiente en el parámetro *phNextProtocol* de la función.
-   Si el archivo DLL del analizador no reconoce los datos no reclamados, el archivo DLL del analizador devuelve el puntero al inicio de los datos no reclamados y Monitor de red continúa intentando analizar los datos no reclamados.

**Para implementar RecognizeFrame**

1.  Pruebe para determinar que reconoce el protocolo.
2.  Si reconoce datos no reclamados y sabe qué protocolo sigue, establezca *pProtocolStatus* en ESTADO DE PROTOCOLO \_ \_ SIGUIENTE \_ PROTOCOLO, establezca *phNextProtocol* en un puntero que apunta al identificador del siguiente protocolo y, a continuación, devuelva un puntero al protocolo siguiente.

    -o bien-

    Si reconoce datos no reclamados y no sabe qué protocolo sigue, establezca *pProtocolStatus* en PROTOCOL \_ STATUS RECOGNIZED y, a continuación, devuelva un puntero al \_ protocolo siguiente.

    -o bien-

    Si reconoce datos no reclamados y el protocolo es el último protocolo de un marco, establezca *pProtocolStatus* en ESTADO DE \_ PROTOCOLO RECLAMADO y, a continuación, devuelva \_ **NULL.**

    -o bien-

    Si no reconoce datos no reclamados, establezca *pProtocolStatus* en PROTOCOL STATUS NOT RECOGNIZED y, a continuación, devuelva el puntero que se le pasa en \_ \_ \_ *pProtocol*.

A continuación se muestra una implementación básica [**de RecognizeFrame.**](recognizeframe.md)

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

 

 



