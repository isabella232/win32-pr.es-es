---
description: Paquete de origen (VS) de SU
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Paquete de origen (VS) de SU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7a3257c11d6d8b42e16d2f066251452bc42a489abe9e666e374a565fa77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072108"
---
# <a name="vaux-source-vs-pack"></a>Paquete de origen (VS) de SU

En las tablas siguientes se muestran los valores utilizados por el controlador MSDV para rellenar el **miembro dwDVVVvSrc** de la [**estructura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obtener más información, [vea DvINFO Field Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

**Dvcr Configuración**



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

CANAL DE TELEVISIÓN (8)

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

CANAL DE TELEVISIÓN (4)

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

STYPE (5)

0:0001

0:0001

0:0000

0:0000

CATEGORÍA DE TUNER (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**DVCPRO 25 y DVCPRO 50 Configuración (planeado)**



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

STYPE (5)

0:0000

0:0000

0:0100

0:0100

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**DVCR 100 Configuración (planeado)**



DV Estándar

DVCPRO 100: planeado

FOURCC

dvh1

Sistema

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

STYPE (5)

1:0100

1:1000

1:0100

VISC (8)

1111:1111

1111:1111

1111:1111

VS Pack

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Comentarios

Los siguientes códigos de campo son de interés:

-   **B/W:** marca en blanco y negro. 1 = color.
-   **50/60:** número de campos.
    -   0 = 60 campos
    -   1 = 50 campos
-   **STYPE:** tipo de señal.

    Definición de IEC 61834:

    -   0:0000 = 525-60 o 625-50, dvsd
    -   0:0001 = 525-60 o 625-50, dvsl (como se define en IEC 61883-5)

    Definición de SMPTE 314M:

    -   0:0000 = compresión 4:1:1
    -   0:0100 = compresión 4:2:2

    Definición de SMPTE 370:

    -   1:0100 = 1080/60i (60 Hz) o 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campo DVINFO Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



