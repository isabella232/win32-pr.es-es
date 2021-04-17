---
description: Paquete de origen de VAUX (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Paquete de origen de VAUX (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f7ad2a91f1be1291b564013041e6dfa23bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687864"
---
# <a name="vaux-source-vs-pack"></a>Paquete de origen de VAUX (VS)

En las tablas siguientes se enumeran los valores utilizados por el controlador MSDV para rellenar el miembro **dwDVVAuxSrc** de la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obtener más información, consulte [configuración de los campos DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**Configuración de DVCR**



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

CANAL DE TV (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

CANAL DE TV (4)

1111

1111

1111

1111

CÓDIGO FUENTE (2)

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

0:0001

0:0001

0:0000

0:0000

CATEGORÍA DE SINTONIZADOR (8)

1111:1111

1111:1111

1111:1111

1111:1111

Paquete de VS

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**Configuración de DVCPRO 25 y DVCPRO 50 (planeada)**



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

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

Reservado (4)

1111

1111

1111

1111

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

0:0100

0:0100

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

Paquete de VS

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**Configuración de DVCR 100 (planeada)**



Estándar DV

DVCPRO 100: planeado

FOURCC

dvh1

System

1080-60i

720-60p

1080-50i

Reservado (8)

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

EN (1)

1

1

1

CLF (2)

11

11

11

Reservado (4)

1111

1111

1111

Reservado (2)

11

11

11

50/60 (1)

0

0

1

SSE ESPERABA UNA (5)

1:0100

1:1000

1:0100

VISC (8)

1111:1111

1111:1111

1111:1111

Paquete de VS

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   **B/W**: marca de blanco y negro. 1 = color.
-   **50/60**: número de campos.
    -   0 = campos 60
    -   1 = campos 50
-   **SSE esperaba una**: tipo de señal.

    Definición de IEC 61834:

    -   0:0000 = 525-60 o 625-50, DVSD
    -   0:0001 = 525-60 o 625-50, DVSL (tal y como se define en IEC 61883-5)

    Definición de 314M SMPTE:

    -   0:0000 = compresión 4:1:1
    -   0:0100 = compresión 4:2:2

    Definición de SMPTE 370:

    -   1:0100 = 1080/60i (60 Hz) o 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configuración del campo DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



