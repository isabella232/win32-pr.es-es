---
description: Paquete de control de código fuente de VAUX (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Paquete de control de código fuente de VAUX (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed51363a15c0024dcaf3edca5d21217cb29396d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911062"
---
# <a name="vaux-source-control-vsc-pack"></a>Paquete de control de código fuente de VAUX (VSC)

En las tablas siguientes se enumeran los valores utilizados por el controlador MSDV para rellenar el miembro **dwDVVAuxCtl** de la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) . Para obtener más información, consulte [configuración de los campos DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md).

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

DISP. (3)

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

GÉNERO (7)

111:1111

111:1111

111:1111

111:1111

Paquete VSC

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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

DISP. (3)

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

Paquete VSC

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**Configuración de DVCPRO 100 (planeada)**



Estándar DV

DVCPRO 100: planeado

FOURCC

dvh1

System

1080-60i

720p: 60p

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

DISP. (3)

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

Paquete VSC

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Observaciones

Los siguientes códigos de campo son de interés:

-   **CGMS**: copiar sistema de administración de generación. 0 = copia permitida sin restricción.

    Los paquetes de VSC reales de la secuencia DV pueden contener valores distintos.

<!-- -->

-   **Modo REC**: modo de grabación. 1 = original.
-   **DISP**: muestra el modo de selección. 000 = 4:3 relación de aspecto, formato completo; 010 = 16:9 relación de aspecto.
-   **BCSYS**: sistema de difusión. Este campo define el tipo de información de señalización de pantalla ancha.
    -   0 = tipo 0 (véase IEC 61880)
    -   1 = tipo 1 (consulte ETSI EN 300 294)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Configuración del campo DVINFO en el controlador MSDV](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



