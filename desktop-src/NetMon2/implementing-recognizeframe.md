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
# <a name="implementing-recognizeframe"></a>Implementación de RecognizeFrame

Monitores de red llama a la función [**RecognizeFrame**](recognizeframe.md) de un analizador para determinar que el analizador reconoce los datos no reclamados de un marco. Los datos no reclamados pueden estar al principio de un fotograma, pero normalmente los datos no reclamados se encuentran en medio de un marco. En la ilustración siguiente se muestran datos no reclamados ubicados en medio de un marco.

![datos no reclamados ubicados en medio de un marco](images/recognizeframe1.png)

Monitor de red proporciona la siguiente información cuando llama a la función [**RecognizeFrame**](recognizeframe.md) :

-   Identificador del marco.
-   Puntero al principio del marco.
-   Puntero al inicio de los datos no reclamados.
-   Valor MAC del primer protocolo del marco.
-   El número de bytes de los datos no reclamados; es decir, los bytes restantes en el marco.
-   Identificador del protocolo anterior.
-   Desplazamiento del protocolo anterior.

Cuando el archivo DLL del analizador determina que los datos no reclamados se inician con el protocolo del analizador, el archivo DLL del analizador determina dónde comienza el siguiente protocolo y qué protocolo sigue. La DLL del analizador funciona de las siguientes maneras condicionales:

-   Si el archivo DLL del analizador reconoce datos no reclamados, el archivo DLL del analizador establece el parámetro *pProtocolStatus* y devuelve un puntero al siguiente protocolo en el marco o **null**. Se devuelve **null** si el protocolo actual es el último protocolo del marco.
-   Si el archivo DLL del analizador reconoce datos no reclamados e identifica el protocolo que sigue (a partir de la información proporcionada en el protocolo), el archivo DLL del analizador devuelve un puntero al identificador del protocolo siguiente en el parámetro *phNextProtocol* de la función.
-   Si el archivo DLL del analizador no reconoce los datos no reclamados, el archivo DLL del analizador devuelve el puntero al inicio de los datos no reclamados y Monitor de red continúa intentando analizar los datos no reclamados.

**Para implementar RecognizeFrame**

1.  Pruebe para determinar que reconoce el protocolo.
2.  Si reconoce datos no reclamados y sabe qué protocolo sigue, establezca *pProtocolStatus* en protocolo \_ \_ siguiente \_ Protocolo, establezca *phNextProtocol* en un puntero que apunte al identificador del siguiente protocolo y, a continuación, devuelva un puntero al protocolo siguiente.

    -o bien-

    Si reconoce datos no reclamados y no sabe qué protocolo sigue, establezca *pProtocolStatus* en estado de protocolo \_ \_ reconocido y, a continuación, devuelva un puntero al protocolo siguiente.

    -o bien-

    Si reconoce datos no reclamados y el protocolo es el último protocolo de un marco, establezca *pProtocolStatus* en estado de \_ Protocolo \_ reclamado y, a continuación, devuelva **null**.

    -o bien-

    Si no reconoce los datos no notificados, establezca *pProtocolStatus* en estado de \_ Protocolo \_ no \_ reconocido y, a continuación, devuelva el puntero que se le pasa en *pProtocol*.

La siguiente es una implementación básica de [**RecognizeFrame**](recognizeframe.md).

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

 

 



