---
description: Paquete de origen (AS) de APACK
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Paquete de origen (AS) de APACK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162494"
---
# <a name="aaux-source-as-pack"></a>Paquete de origen (AS) de APACK

En las tablas siguientes se muestran los valores utilizados por el controlador MSDV para rellenar los **miembros dwDVAJdbcSrc** y **dwDVAJdbcSrc1** de la [**estructura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obtener más información, [vea DVINFO Field Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

Dvcr Configuración



DV Estándar

DVCR (IEC 61834)

FOURCC

dvsl

dvsd

Sistema

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

AF SIZE (6)

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

MODO AUDIO (4)

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

STYPE (5)

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

PAQUETE DE AS

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



 

DVCR 25 y DVCPRO 50 Configuración (planeado)



DV Estándar

DVCPRO (SMPTE 314M): planeado

FOURCC

dv25

dv50

Sistema

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

AF SIZE (6)

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

MODO AUDIO (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

0001

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

STYPE (5)

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

PAQUETE DE AS

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
> \* La [**estructura DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) contiene dos paquetes as de APACK, para los bloques de audio 1 y 2. DV50 tiene cuatro bloques de audio; Los bloques 3 y 4 no se representan en la **estructura DVINFO.**

 

DVCR 100 Configuración (planeado)



DV Estándar

DVCPRO 100: planeado

FOURCC

dvh1

Sistema

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

AF SIZE (6)

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

MODO AUDIO (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

Reservado (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

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

PAQUETE DE AS

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \*DVCPRO 100 tiene 8 bloques de audio; Los bloques del 3 al 8 no se representan en la [estructura DVINFO.](dvinfo-field-settings-in-the-msdv-driver.md)

 

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   LF: marca de modo bloqueado. Indica si el audio está bloqueado.
    -   0 = Bloqueado
    -   1 = Desbloqueado
-   AF SIZE: tamaño del marco de audio. Especifica el número de muestras de audio por fotograma.

    Definición iec 61834:

    -   00:1111 = 1068 muestras por fotograma
    -   01:0000 = 1280 muestras por fotograma

    Definición de SMPTE 314M:

    -   01:0110 = 1602 muestras por fotograma
    -   01:1000 = 1920 muestras por fotograma

    En función de la velocidad de fotogramas, el número exacto de muestras de un fotograma puede variar. Por ejemplo, PRESS es de 30 000/1001 fotogramas por segundo (29,97 fps). Con audio de 32 kHz, hay aproximadamente 1067,73 muestras de audio por fotograma. Por lo tanto, la tasa nominal es 1068, pero el número real varía por fotograma. Además, con el audio desbloqueado, el número de muestras de audio por fotograma puede variar dentro de un intervalo determinado a lo largo del tiempo.

<!-- -->

-   SM: modo estéreo.
    -   0 = Estéreo
    -   1 = Mono
-   CHN: número de canales de audio por bloque de audio.
    -   0 = Un canal por bloque de audio
    -   1 = Dos canales por bloque de audio
-   MODO AUDIO: indica el contenido de la señal de audio en cada canal. La interpretación de este campo depende de qué valores se colocan en los campos SM y CHN. Las definiciones que se indican a continuación son para los valores usados por MSDV; consulte las especificaciones para obtener más información.

    Definición iec 61834:

    -   0000 = Ch a/c/e/g es el canal izquierdo, Ch b/d/f/h es el canal derecho
    -   1111 = sin datos de audio

    Definición de SMPTE 314M:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: número de campos.
    -   0 = 60 campos
    -   1 = 50 campos
-   STYPE: tipo de sistema.

    Definición iec 61834:

    -   00000 = 525-60 o 625-50, dvsd
    -   00001 = 525-60 o 625-50, dvsl (vea IEC 61883-5)

    Definición de SMPTE 314M/SPMTE 370:

    -   00000 = 2 bloques de audio por fotograma de vídeo
    -   00010 = 4 bloques de audio por fotograma de vídeo
    -   00011 = 8 bloques de audio por fotograma de vídeo

-   SMP: frecuencia de muestreo.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU: cuantificación.
    -   0 = 16 bits lineales
    -   1 = 12 bits no lineales

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campos DVINFO Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



