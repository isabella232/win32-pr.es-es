---
description: Paquete de control de código fuente de AAUX (ASC)
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Paquete de control de código fuente de AAUX (ASC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806536"
---
# <a name="aaux-source-control-asc-pack"></a>Paquete de control de código fuente de AAUX (ASC)

En las tablas siguientes se enumeran los valores usados por el controlador MSDV para rellenar el **dwDVAAuxCtl** y

**dwDVAAuxCtl1** miembros de la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obtener más información, consulte [configuración de los campos DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

INSERTAR CH (3)

111

111

111

111

DRF (1)

1

1

1

1

VELOCIDAD (7)

010:0000

010:0000

010:0000

010:0000

Reservado (1)

1

1

1

1

GÉNERO (7)

111:1111

111:1111

111:1111

111:1111

ASC Pack (ambos bloques de audio)\*

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F

0xFFA0CF3F



 

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

ATENUAR ST (1)

1

1

1

1

FIN DE DESVANECIMIENTO (1)

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

VELOCIDAD (7)

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



 

\* La estructura *DVINFO* contiene dos AAUX como paquetes, para los bloques de audio 1 y 2. DV50 tiene cuatro bloques de audio; los bloques 3 y 4 no se representan en la estructura *DVINFO* .

Configuración de DVCR 100 (planeada)



Estándar DV

DVCPRO 100: planeado

FOURCC

dvh1

System

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

ATENUAR ST (1)

1

1

1

FIN DE DESVANECIMIENTO (1)

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

VELOCIDAD (7)

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



 

\* DVCPRO 100 tiene ocho bloques de audio; los bloques 3 a 8 no se representan en la estructura *DVINFO* .

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   **CGMS**: copiar sistema de administración de generación. 0 = copia permitida sin restricción.

    Los módulos de ASC reales en el flujo DV pueden contener valores distintos.

<!-- -->

-   **Modo REC**: modo de grabación. 1 = original
-   **Velocidad**: velocidad de reproducción del VTR.

    Definición de IEC 61834:

    -   010:0000 = velocidad normal, 525-60 o 625-50

    Definición de 314M SMPTE:

    -   111:1000 = velocidad normal, 525-60
    -   110:0100 = velocidad normal, 625-50

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configuración del campo DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



