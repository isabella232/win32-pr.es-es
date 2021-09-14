---
description: Emisión de comandos de AV/C sin formato
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emisión de comandos de AV/C sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063231"
---
# <a name="issuing-raw-avc-commands"></a>Emisión de comandos de AV/C sin formato

Las interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)y [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funcionan traduciendo las llamadas de método en comandos para el controlador y, a continuación, interpretando la respuesta del controlador y devolviendola a través de **un HRESULT** o un parámetro de salida. Sin embargo, es posible que algunas funciones de dispositivo no sean accesibles a través de estos métodos. Por lo tanto, MSDV admite el envío de comandos AV/C sin procesar al dispositivo.

Debe tener en cuenta los siguientes puntos al usar esta característica:

-   El comando se pasa directamente al dispositivo, sin comprobación de errores ni validación de parámetros. Por esta razón, debe emitir comandos de AV/C sin procesar solo cuando las interfaces DirectShow no implementen la funcionalidad que necesita.
-   Todos los comandos de AV/C sin procesar son sincrónicos. El subproceso que emite el comando se bloquea hasta que se devuelve el comando.
-   Solo se puede dar un comando a la vez. Mientras se procesa el comando, el dispositivo rechazará los comandos adicionales.
-   El controlador UVC no admite comandos AV/C sin procesar.

Para enviar un comando de AV/C, formatee el comando como una matriz de bytes. A [**continuación, llame a IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Pase la marca ED \_ RAW \_ EXT \_ DEV \_ CMD, el tamaño de la matriz y la matriz. Debe convertir la dirección de la matriz en un **tipo LPOLESTR, \*** porque el propósito original de este parámetro era devolver un valor de cadena.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR*) AvcCmd);
```



El contenido de la matriz se pasa directamente al dispositivo, por lo que debe tener cuidado de formatearlo correctamente. Un comando puede tener como destino la unidad (cámara) o una subunidad (cinta o cámara). Los estándares pertinentes están disponibles en el sitio web de la asociación comercial [1394](https://1394ta.org).

-   Especificación general del conjunto de comandos de la interfaz digital de AV/C
-   AV/C Tape Recorder/Player Subunit Specification

En la primera se describe cómo dar formato a los comandos de AV/C y se enumeran los comandos de unidad. En esta última especificación se enumeran los comandos de subunidad.

El **método GetTransportBasicParameters** puede devolver uno de los siguientes códigos de error:



| Código de error              | Descripción                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| TIEMPO DE ESPERA \_ DE ERROR          | Se ha producido un tiempo de espera del comando.                                                           |
| ERROR \_ REQ \_ NOT \_ ACCEP  | El dispositivo no aceptó el comando.                                           |
| ERROR \_ NO \_ ADMITIDO   | El dispositivo no admite el comando .                                         |
| SOLICITUD DE ERROR \_ \_ ANULADA | Se anuló el comando. Possbly the device was removed or a bus reset occurred. |



 

> [!Note]  
> Estos errores se devuelven como códigos de error de Win32, no COMO HDU, por lo que debe probar estos valores directamente, en lugar de usar las macros **SUCCEEDED** y **FAILED.**

 

Si el método devuelve S \_ OK, la respuesta del dispositivo se copia en la matriz. La carga de respuesta puede ser mayor que el comando, por lo que debe asignar un búfer lo suficientemente grande como para contenerlo. El tamaño máximo de carga es de 512 bytes. Tenga en cuenta que un valor devuelto de S \_ OK no siempre significa que el dispositivo haya realizado correctamente el comando. La aplicación debe examinar la carga de respuesta para determinar el estado.

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

[Control de una cámara de vídeo dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



