---
description: Paquete de origen (AS) de AAUX
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Paquete de origen (AS) de AAUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274789"
---
# <a name="aaux-source-as-pack"></a>Paquete de origen (AS) de AAUX

En las tablas siguientes se enumeran los valores utilizados por el controlador MSDV para rellenar los miembros **dwDVAAuxSrc** y **dwDVAAuxSrc1** de la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obtener más información, consulte [configuración de los campos DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

Configuración de DVCR



Estándar DV

DVCR (IEC 61834)

FOURCC

dvsl

dvsd

System

525-60

625-50

525-60

625-50

LF (1)

1

1

1

1

Reservado (1)

1

1

1

1

TAMAÑO AF (6)

00:1111

01:0000

00:1111

01:0000

SM (1)

0

0

0

0

CHN (2)

01

01

01

01

PA (1)

1

1

1

1

MODO DE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

Reservado (1)

1

1

1

1

ML (1)

1

1

1

1

50/60 (1)

0

1

0

1

SSE ESPERABA UNA (5)

0:0001

0:0001

0:0000

0:0000

EF (1)

1

1

1

1

TC (1)

1

1

1

1

SMP (3)

010

010

010

010

QU (3)

001

001

001

001

Paquete de AS

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

Configuración de DVCR 25 y DVCPRO 50 (planeada)



Estándar DV

DVCPRO (SMPTE 314M): planeado

FOURCC

dv25

dv50

System

525-60

625-50

525-60

625-50

LF (1)

0

0

0

0

Reservado (1)

1

1

1

1

TAMAÑO AF (6)

01:0110

01:1000

01:0110

01:1000

Reservado (1)

0

0

0

0

CHN (2)

00

00

00

00

Reservado (1)

1

1

1

1

MODO DE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0,001

0,001

0,001

0,001

Reservado (2)

11

11

11

11

50/60 (1)

0

1

0

1

SSE ESPERABA UNA (5)

0:0000

0:0000

0:0010

0:0010

Reservado (2)

11

11

11

11

SMP (3)

000

000

000

000

QU (3)

000

000

000

000

Paquete de AS

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \* La estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contiene dos AAUX como paquetes, para los bloques de audio 1 y 2. DV50 tiene cuatro bloques de audio; los bloques 3 y 4 no se representan en la estructura **DVINFO** .

 

Configuración de DVCR 100 (planeada)



Estándar DV

DVCPRO 100: planeado

FOURCC

dvh1

System

1080-60i

720-60p

1080-50i

LF (1)

0

0

0

Reservado (1)

1

1

1

TAMAÑO AF (6)

01:0110

01:0110

01:1000

Reservado (1)

0

0

0

CHN (2)

00

00

00

Reservado (1)

1

1

1

MODO DE AUDIO (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0,001

0,001

0,001

Reservado (2)

11

11

11

50/60 (1)

0

0

1

SSE ESPERABA UNA (5)

0:0011

0:0011

0:0011

Reservado (2)

11

11

11

SMP (3)

000

000

000

QU (3)

000

000

000

Paquete de AS

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* DVCPRO 100 tiene ocho bloques de audio; los bloques 3 a 8 no se representan en la estructura [DVINFO](dvinfo-field-settings-in-the-msdv-driver.md) .

 

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   LF: marca de modo bloqueado. Indica si el audio está bloqueado.
    -   0 = bloqueado
    -   1 = desbloqueado
-   AF SIZE: tamaño del fotograma de audio. Especifica el número de muestras de audio por fotograma.

    Definición de IEC 61834:

    -   00:1111 = 1068 ejemplos por fotograma
    -   01:0000 = 1280 ejemplos por fotograma

    Definición de 314M SMPTE:

    -   01:0110 = 1602 ejemplos por fotograma
    -   01:1000 = 1920 ejemplos por fotograma

    En función de la velocidad de fotogramas, el número exacto de muestras de un fotograma puede variar. Por ejemplo, NTSC es 30000/1001 fotogramas por segundo (29,97 fps). Con audio de 32 kHz, hay aproximadamente 1067,73 muestras de audio por fotograma. Por lo tanto, la tasa nominal es 1068, pero el número real varía según el fotograma. Además, con audio desbloqueado, se permite que el número de muestras de audio por fotograma varíe dentro de un intervalo determinado a lo largo del tiempo.

<!-- -->

-   SM: modo estéreo.
    -   0 = estéreo
    -   1 = mono
-   CHN: número de canales de audio por bloque de audio.
    -   0 = un canal por bloque de audio
    -   1 = dos canales por bloque de audio
-   MODO de AUDIO: indica el contenido de la señal de audio en cada canal. La interpretación de este campo depende de los valores que se colocan en los campos SM y CHN. Las definiciones que se indican a continuación son para los valores usados por MSDV; Consulte las especificaciones para obtener más información.

    Definición de IEC 61834:

    -   0000 = CH a/c/e/g es el canal izquierdo, CH b/d/f/h es el canal derecho
    -   1111 = sin datos de audio

    Definición de 314M SMPTE:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: número de campos.
    -   0 = campos 60
    -   1 = campos 50
-   SSE esperaba una: tipo de sistema.

    Definición de IEC 61834:

    -   00000 = 525-60 o 625-50, DVSD
    -   00001 = 525-60 o 625-50, DVSL (véase IEC 61883-5)

    Definición 370 de SMPTE 314M/SPMTE:

    -   00000 = 2 bloques de audio por fotograma de vídeo
    -   00010 = 4 bloques de audio por fotograma de vídeo
    -   00011 = 8 bloques de audio por fotograma de vídeo

-   SMP: frecuencia de muestreo.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU: cuantificación.
    -   0 = 16 bits lineal
    -   1 = 12 bits no lineal

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configuración del campo DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



