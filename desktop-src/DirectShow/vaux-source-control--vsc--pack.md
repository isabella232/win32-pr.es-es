---
description: Paquete de control de código fuente (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Paquete de control de código fuente (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072079"
---
# <a name="vaux-source-control-vsc-pack"></a>Paquete de control de código fuente (VSC)

En las tablas siguientes se muestran los valores utilizados por el controlador MSDV para rellenar el **miembro dwDVVCtl de** la [**estructura DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo) Para obtener más información, [vea Dvinfo Field Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

Reservado (1)

1

1

1

1

MODO REC (2)

00

00

00

00

Reservado (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

ST (1)

1

1

1

1

SC (1)

1

1

1

1

BCSYS (2)

00

01

00

01

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

VSC Pack

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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

CGMS (2)

00

00

00

00

Reservado (6)

11:1111

11:1111

11:1111

11:1111

Reservado (2)

11

11

11

11

Reservado (2)

00

00

00

00

Reservado (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

Reservado (2)

11

11

11

11

Reservado (2)

00

00

00

00

Reservado (8)

1111:1111

1111:1111

1111:1111

1111:1111

VSC Pack

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**DVCPRO 100 Configuración (planeado)**



DV Estándar

DVCPRO 100: planeado

FOURCC

dvh1

Sistema

1080-60i

720p-60p

1080-50i

CGMS (2)

00

00

00

Reservado (6)

11:1111

11:1111

11:1111

Reservado (2)

11

11

11

Reservado (2)

00

00

00

Reservado (1)

1

1

1

DISP (3)

010

010

010

FF (1)

1

1

1

FS (1)

1

1

1

FC (1)

1

1

1

IL (1)

1

1

1

Reservado (2)

11

11

11

Reservado (2)

00

00

00

Reservado (8)

1111:1111

1111:1111

1111:1111

VSC Pack

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Comentarios

Los siguientes códigos de campo son de interés:

-   **CGMS:** sistema de administración de generación de copias. 0 = se permite copiar sin restricciones.

    Los paquetes de VSC reales en la secuencia DV pueden contener valores diferentes.

<!-- -->

-   **REC MODE**: modo de grabación. 1 = Original.
-   **DISP:** mostrar el modo de selección. 000 = relación de aspecto 4:3, formato completo; 010 = relación de aspecto 16:9.
-   **BCSYS:** sistema de difusión. Este campo define el tipo de información de señalización de pantalla ancha.
    -   0 = tipo 0 (vea IEC 61880)
    -   1 = tipo 1 (vea ETSI EN 300 294)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Campo DVINFO Configuración en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



