---
description: Paquete de control de código fuente (ASC) de AJUN
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Paquete de control de código fuente (ASC) de AJUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162493"
---
# <a name="aaux-source-control-asc-pack"></a>Paquete de control de código fuente (ASC) de AJUN

En las tablas siguientes se muestran los valores utilizados por el controlador MSDV para rellenar **dwDVACtl y** .

**Miembros dwDVACtlCtl1** de la [**estructura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obtener más información, [vea DvINFO Field Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

DVCR Configuración



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

CGMS (2)

00

00

00

00

ISR (2)

11

11

11

11

CMP (2)

11

11

11

11

SS (2)

11

11

11

11

REC ST (1)

1

1

1

1

REC END (1)

1

1

1

1

MODO REC (3)

001

001

001

001

INSERT CH (3)

111

111

111

111

DRF (1)

1

1

1

1

SPEED (7)

010:0000

010:0000

010:0000

010:0000

Reservado (1)

1

1

1

1

GENRE (7)

111:1111

111:1111

111:1111

111:1111

ASC Pack (ambos bloques de audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

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

CGMS (2)

00

00

00

00

Reservado (4)

1111

1111

1111

1111

EFC (2)

00

00

00

00

REC ST (1)

1

1

1

1

REC END (1)

1

1

1

1

FADE ST (1)

1

1

1

1

FADE END (1)

1

1

1

1

Reservado (4)

1111

1111

1111

1111

DRF (1)

1

1

1

1

SPEED (7)

111:1000

110:0100

111:1000

110:0100

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

ASC Pack (ambos bloques de audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

\* La *estructura DVINFO* contiene dos paquetes as de APACK, para los bloques de audio 1 y 2. DV50 tiene cuatro bloques de audio; Los bloques 3 y 4 no se representan en la *estructura DVINFO.*

DVCR 100 Configuración (planeado)



DV Estándar

DVCPRO 100: planeado

FOURCC

dvh1

Sistema

1080-60i

720-60p

1080-50i

CGMS (2)

00

00

00

Reservado (4)

1111

1111

1111

EFC (2)

00

00

00

REC ST (1)

1

1

1

REC END (1)

1

1

1

FADE ST (1)

1

1

1

FADE END (1)

1

1

1

Reservado (4)

1111

1111

1111

DRF (1)

1

1

1

SPEED (7)

111:1000

111:1000

110:0100

Reservado (8)

1111:1111

1111:1111

1111:1111

ASC Pack (ambos bloques de audio)\*

0xFFF8FF3C

0xFFF8FF3C

0xFFE4FF3C



 

\*DVCPRO 100 tiene 8 bloques de audio; Los bloques del 3 al 8 no se representan en la *estructura DVINFO.*

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   **CGMS:** sistema de administración de generación de copias. 0 = se permite copiar sin restricciones.

    Los paquetes de ASC reales de la secuencia DV pueden contener valores diferentes.

<!-- -->

-   **REC MODE**: modo de grabación. 1 = Original
-   **SPEED:** velocidad de reproducción de VTR.

    Definición de IEC 61834:

    -   010:0000 = velocidad normal, 525-60 o 625-50

    Definición de SMPTE 314M:

    -   111:1000 = velocidad normal, 525-60
    -   110:0100 = velocidad normal, 625-50

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campo DVINFO Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



