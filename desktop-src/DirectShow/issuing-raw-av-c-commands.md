---
description: Emisión de comandos AV/C sin formato
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emisión de comandos AV/C sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422844"
---
# <a name="issuing-raw-avc-commands"></a>Emisión de comandos AV/C sin formato

Las interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)y [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funcionan mediante la traducción de las llamadas de método en comandos para el controlador y, a continuación, la interpretación de la respuesta del controlador y su devolución a través de un **valor HRESULT** o un parámetro de salida. Sin embargo, es posible que algunas funciones del dispositivo no sean accesibles a través de estos métodos. Por lo tanto, MSDV admite el envío de comandos AV/C sin formato al dispositivo.

Debe tener en cuenta los siguientes puntos al usar esta característica:

-   El comando se pasa directamente al dispositivo, sin comprobación de errores o validación de parámetros. Por esta razón, debe emitir comandos AV/C sin procesar solo cuando las interfaces de DirectShow no implementan la funcionalidad que necesita.
-   Todos los comandos AV/C sin procesar son sincrónicos. El subproceso que emite el comando se bloquea hasta que el comando devuelve.
-   Solo se puede proporcionar un comando cada vez. Mientras se está procesando el comando, el dispositivo rechazará los comandos adicionales.
-   El controlador UVC no admite comandos AV/C sin formato.

Para enviar un comando AV/C, formatee el comando como una matriz de bytes. Después, llame a [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Pase la marca ED \_ raw \_ ext \_ dev \_ cmd, el tamaño de la matriz y la matriz. Debe convertir la dirección de matriz en un tipo ** \* LPOLESTR* _, porque el propósito original de este parámetro era devolver un valor de cadena.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



El contenido de la matriz se pasa directamente al dispositivo, por lo que debe tener cuidado de formatearlo correctamente. Un comando puede tener como destino la unidad (videocámara) o una subunidad (cinta o cámara). Los estándares pertinentes están disponibles en el [sitio web de la asociación comercial 1394](https://1394ta.org).

-   Especificación general del conjunto de comandos de la interfaz digital AV/C
-   Grabadora de cinta AV/C/especificación de subunidad del reproductor

En el primer procedimiento se describe cómo dar formato a los comandos AV/C y se enumeran los comandos de la unidad. La última especificación muestra los comandos de la subunidad.

El método **GetTransportBasicParameters** puede devolver uno de los siguientes códigos de error:



| Código de error              | Descripción                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| tiempo de espera de ERROR \_          | El comando agotó el tiempo de espera.                                                           |
| ERROR \_ req \_ no \_ ACCEP  | El dispositivo no aceptó el comando.                                           |
| ERROR \_ no \_ admitido   | El dispositivo no admite el comando.                                         |
| solicitud de ERROR \_ \_ anulada | El comando se anuló. Possbly el dispositivo se quitó o se produjo un restablecimiento de bus. |



 

> [!Note]  
> Estos errores se devuelven como códigos de error de Win32, no como HRESULT, por lo que debe probar estos valores directamente, en lugar de usar las macros **Succeeded** y **failed** .

 

Si el método devuelve S \_ correcto, la respuesta del dispositivo se copia en la matriz. La carga útil de respuesta puede ser mayor que el comando, por lo que debe asignar un búfer lo suficientemente grande como para almacenarlo. El tamaño máximo de carga es de 512 bytes. Tenga en cuenta que un valor devuelto de S \_ OK no siempre significa que el dispositivo ha realizado correctamente el comando. La aplicación debe examinar la carga de respuesta para determinar el estado.

En el ejemplo siguiente se muestra el comando para buscar una búsqueda de número de pista absoluta:


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



