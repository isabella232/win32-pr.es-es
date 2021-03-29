---
description: Envío de solicitudes de estado de COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Envío de solicitudes de estado de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805210"
---
# <a name="sending-copp-status-requests"></a>Envío de solicitudes de estado de COPP

Para enviar una solicitud de estado del Protocolo de protección de la salida (COPP), rellene una estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) con los datos de la solicitud. Los miembros de la estructura son:

-   **rApp**. Número aleatorio de 128 bits, escrito como un GUID. Se devuelve el mismo número en la respuesta del controlador. Debe asignar el número aleatorio en el montón y, a continuación, copiarlo en la estructura. Esto protege contra los ataques en los que el atacante modifica el contenido de la estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .
-   **guidStatusRequestID**. GUID que identifica la solicitud. Consulte [referencia de consulta de COPP](copp-query-reference.md).
-   **dwSequence**. El número de secuencia de estado. Incremente este valor después de cada solicitud de estado. (En la sección [Inicio de una sesión de COPP](initiating-a-copp-session.md), este valor se muestra como *uStatusSeq* en los ejemplos de código).
-   **cbSizeData**. Tamaño, en bytes, de los datos adicionales necesarios para la solicitud.
-   **StatusData**. Datos de la solicitud de estado.

Pase la estructura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) al método [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) . Por ejemplo, el código siguiente envía una solicitud de estado que consulta qué mecanismos de protección están disponibles:


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



La respuesta se escribe en el miembro **COPPStatus** de la estructura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) . El tamaño de los datos válidos en la respuesta se proporciona en el miembro **cbSizeData** . Para garantizar la integridad del mensaje, el controlador calcula un código de autenticación de mensajes (MAC) mediante el algoritmo OMAC 1 y devuelve este valor en el miembro **macKDI** de la estructura. La aplicación debe comprobar este valor de la siguiente manera:

1.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **macKDI** de la estructura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (es decir, **cbSizeData** más **COPPStatus**).
2.  Compare esta etiqueta con el valor de **macKDI**, con un **memcmp** recto.

El algoritmo OMAC 1 se describe en detalle en [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . COPP usa los siguientes parámetros de OMAC-1:

-   E = AES
-   t = 128 bits

Los datos devueltos por la solicitud de estado siempre comienzan con dos elementos:

-   El mismo valor de **rApp** pasado por la aplicación. Debe comprobar que este valor coincide con el valor original almacenado en el montón.
-   Un valor de [**COPP \_ StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) que indica si el estado de protección de salida ha cambiado.

Dado que se puede perder o volver a configurar la conexión, la aplicación debe sondear periódicamente el estado actual del controlador. Si \_ se establece la marca RenegotiationRequired de COPP, la aplicación debe intentar restablecer el nivel de protección. Si \_ se establece la marca LinkLost de COPP, la aplicación debe detener la reproducción del contenido. Por ejemplo, \_ se puede devolver la marca LinkLost de COPP porque el usuario desconectó el conector de salida. La aplicación debe liberar la instancia actual de VMR, crear una nueva instancia de VMR y establecer una nueva sesión de COPP (incluido el intercambio de claves y la validación de certificados).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



