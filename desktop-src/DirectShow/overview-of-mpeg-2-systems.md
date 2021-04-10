---
description: Información general de los sistemas MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Información general de los sistemas MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152504"
---
# <a name="overview-of-mpeg-2-systems"></a>Información general de los sistemas MPEG-2

En esta sección se ofrece una descripción general no técnica de la capa de sistemas MPEG-2. MPEG-2 es el estándar que define cómo se multiplexan las secuencias de audio y vídeo en MPEG-2.

**Flujos elementales**

La multiplexación MPEG-2 comienza con uno o varios flujos de bytes, denominados secuencias elementales, que contienen vídeo, audio u otros datos. Por ejemplo, un vídeo ES contiene fotogramas de vídeo comprimidos, más encabezados de secuencia, encabezados de grupo de imágenes (GOP) y cualquier otro elemento que necesite el descodificador para descodificar la secuencia. La capa de sistemas no define el contenido de la secuencia de bytes ES.

Una secuencia elemental se divide en paquetes, formando una *secuencia elemental* (PES) con paquetes. Los paquetes PES tienen una longitud variable. El contenido del paquete se denomina *carga*. Cada paquete de PES también incluye un encabezado. El multiplexor asigna un identificador de secuencia de 1 byte a cada PES; los paquetes PES individuales se identifican mediante el identificador de secuencia en el encabezado del paquete. En el caso de las secuencias de audio, el ID. de secuencia tiene el formato 110 *xxxxx*. En el caso de vídeo, el ID. de secuencia tiene el formato 1110 *AAAA*.

El estándar MPEG-2 define dos maneras de proporcionar flujos elementales con paquetes: *secuencias de programa* y secuencias de *transporte*.

**Flujos de programa**

Los flujos de programa están diseñados para entornos que no tienen errores relativamente, como el almacenamiento de archivos local. En una secuencia de programa, los paquetes de PES se multiplexan y se organizan en unidades denominadas *paquetes*. Todas las secuencias de PES en una secuencia de programa se sincronizan con el mismo reloj.

**Flujos de transporte**

Los flujos de transporte (TS) están diseñados para entornos no confiables o propensos a errores, como difusiones de red. Además, pueden contener varios programas que se sincronizan con distintos relojes. Un flujo de transporte agrega una segunda capa de empaquetado: los flujos de PES se empaquetan dentro de los paquetes de flujo de transporte, que tienen un tamaño fijo de 188 bytes por paquete. Los paquetes de TS también pueden contener secuencias de información del programa, que se describen en la sección siguiente.

Cada paquete de TS tiene un encabezado de 4 bytes, más un campo de adaptación opcional que contiene información de encabezado adicional. El multiplexor asigna un identificador de programa (PID) a cada secuencia de PES o de información de programa. Los PID se usan para identificar los paquetes de TS, de manera similar a la forma en que los identificadores de flujo identifican los paquetes de PES. (Si una secuencia de transporte contiene varios programas, es posible que los identificadores de *flujo* no sean únicos, pero las asignaciones de PID son únicas en el flujo de transporte).

**Información específica del programa**

Dado que una secuencia de transporte puede llevar varios programas, debe haber una manera de asociar los distintos paquetes de PES con los programas a los que pertenecen. Esto se logra mediante el uso de tablas que identifican los flujos de programa. Colectivamente, estos datos se denominan información específica del programa (PSI). Los datos de la PSI se transfieren en paquetes de TS, al igual que los datos de PES. Hay varios tipos de datos de PSI, entre los que se incluyen:

-   Tabla de Asociación de programas (PAT). PAT siempre se asigna al PID 0x000. Cada entrada de la PAT es un PID que identifica los paquetes de pago para ese programa (vea el elemento siguiente).
-   Tabla de asignación de programa (PMT). Cada pago define un programa. La función PMT contiene una lista de secuencias; cada entrada de tabla proporciona el PID para esa secuencia, más un código que identifica el tipo de flujo. ISO/IEC 13818-1 define algunos tipos de flujo estándar; en la tabla siguiente se muestra una lista abreviada.

    | tipo de secuencia \_ | Descripción  |
    |--------------|--------------|
    | 0x01         | Vídeo MPEG-1 |
    | 0x02         | Vídeo MPEG-2 |
    | 0x03         | Audio MPEG-1 |
    | 0x04         | Audio MPEG-2 |
    | 0x80-0xFF  | Usuario privado |

    

     

    Otros estándares basados en MPEG-2, como ATSC, pueden definir tipos de flujo adicionales en el intervalo "usuario privado". Por ejemplo, ATSC define 0x81 como audio de Dolby AC-3.

-   Tablas de acceso condicional (CAT)
-   Tablas de identificación de red (nits)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



