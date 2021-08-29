---
description: Introducción a los sistemas MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Introducción a los sistemas MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36b0ce6d98024187c9f194065520d388406f4feb95af6fd4df43b7a79e244e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148558"
---
# <a name="overview-of-mpeg-2-systems"></a>Introducción a los sistemas MPEG-2

En esta sección se proporciona información general y no técnica de la capa de sistemas MPEG-2. Mpeg-2 Systems es el estándar que define cómo se multiplexa la secuencia de audio y vídeo en MPEG-2.

**Secuencias**

La multiplexación MPEG-2 comienza con una o varias secuencias de bytes, denominadas secuencias elementales (ES), que contienen vídeo, audio u otros datos. Por ejemplo, una ES de vídeo contiene fotogramas de vídeo comprimidos, además de encabezados de secuencia, encabezados de grupo de imágenes (GOP) y cualquier otra cosa que necesite el descodificador para descodificar la secuencia. La capa De sistemas no define el contenido de la secuencia de bytes de ES.

Una secuencia elemental se divide en paquetes, formando *una* secuencia elemental en paquetes (PES). Los paquetes PES tienen una longitud variable. El contenido del paquete se denomina *carga*. Cada paquete PES también incluye un encabezado . El multiplexor asigna un identificador de secuencia de 1 byte a cada PES; Los paquetes PES individuales se identifican mediante el identificador de flujo en el encabezado del paquete. Para las secuencias de audio, el identificador de flujo tiene el formato 110 *xxxxx*. Para el vídeo, el identificador de flujo tiene el formato 1110 *yyyy*.

El estándar MPEG-2 define dos maneras de entregar secuencias elementales en paquetes: *secuencias de* programa y *secuencias de transporte.*

**Programa Secuencias**

Los flujos de programa están diseñados para entornos relativamente sin errores, como el almacenamiento de archivos local. En una secuencia de programa, los paquetes PES se multiplexa y se organizan en unidades denominadas *paquetes*. Todas las secuencias PES de una secuencia de programa se sincronizan con el mismo reloj.

**Transporte Secuencias**

Las secuencias de transporte (TS) están diseñadas para entornos poco confiables o propensos a errores, como las difusión de red. Además, pueden contener varios programas que se sincronizan con distintos relojes. Una secuencia de transporte agrega una segunda capa de paquetes: las secuencias PES se empaquetan dentro de paquetes de flujo de transporte, que tienen un tamaño fijo de 188 bytes por paquete. Los paquetes TS también pueden contener secuencias de información del programa, que se describen en la sección siguiente.

Cada paquete de TS tiene un encabezado de 4 bytes, además de un campo de adaptación opcional que contiene información de encabezado adicional. El multiplexor asigna un identificador de programa (PID) a cada secuencia PES o flujo de información del programa. Los PID se usan para identificar los paquetes TS, de forma similar a la manera en que los id. de flujo identifican los paquetes PES. (Si una secuencia de transporte  contiene varios programas, es posible que los identificadores de secuencia no sean únicos, pero las asignaciones de PID son únicas dentro de la secuencia de transporte).

**Información específica del programa**

Dado que una secuencia de transporte puede llevar varios programas, debe haber una manera de asociar los distintos paquetes PES con los programas a los que pertenecen. Esto se logra mediante tablas que identifican las secuencias del programa. En conjunto, estos datos se denominan información específica del programa (PSI). Los datos de PSI se llevan en paquetes TS, al igual que los datos PES. Hay varios tipos de datos PSI, entre los que se incluyen:

-   Tabla de asociación de programas (PAT). El PAT siempre se asigna a pid 0x000. Cada entrada del PAT es un PID que identifica los paquetes PMT para ese programa (consulte el siguiente elemento).
-   Tabla de asignación de programa (PMT). Cada PMT define un programa. El PMT contiene una lista de secuencias; cada entrada de tabla proporciona el PID para esa secuencia, además de un código que identifica el tipo de secuencia. ISO/IEC 13818-1 define algunos tipos de secuencia estándar; En la tabla siguiente se muestra una lista abreviada.

    | tipo \_ de secuencia | Descripción  |
    |--------------|--------------|
    | 0x01         | Vídeo MPEG-1 |
    | 0x02         | Vídeo MPEG-2 |
    | 0x03         | Audio MPEG-1 |
    | 0x04         | Audio MPEG-2 |
    | 0x80: 0xFF  | Usuario privado |

    

     

    Otros estándares basados en MPEG-2, como ATSC, pueden definir tipos de secuencias adicionales en el intervalo "usuario privado". Por ejemplo, ATSC define 0x81 audio Dolby AC-3.

-   Tablas de acceso condicional (CAT)
-   Tablas de identificación de red (NIT)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



