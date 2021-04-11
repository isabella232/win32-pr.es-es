---
description: La tecnología de memoria persistente (PM) proporciona acceso de nivel de bytes a medios no volátiles, a la vez que reduce la latencia del almacenamiento o la recuperación de datos de forma significativa.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: 'Programación de memoria persistente en Windows: integración de NVML'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278917"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programación de memoria persistente en Windows: integración de NVML

La tecnología de memoria persistente (PM) proporciona acceso de nivel de bytes a medios no volátiles, a la vez que reduce la latencia del almacenamiento o la recuperación de datos de forma significativa. Crea un nuevo nivel entre la memoria del sistema y el almacenamiento tradicional. Cualquier programa que dependa o escale con escrituras rápidas en un medio persistente puede beneficiarse de PM.

El propósito de este artículo es describir cómo se puede integrar la biblioteca de memoria no volátil (NVML) en un proyecto de Visual Studio para facilitar su uso.

> [!Note]  
> La memoria persistente a veces se conoce también como memoria de clase de almacenamiento (SCM).

 

## <a name="pm-and-nvml"></a>PM y NVML

La primera compatibilidad con la memoria persistente se incorporó en Windows Server 2016 y la actualización de aniversario de Windows 10 (1607). Para obtener una introducción rápida, eche un vistazo a estos dos vídeos de Channel9:

-   [Uso de memoria no volátil (NVDIMM-N) como almacenamiento en bloque en Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Uso de memoria no volátil (NVDIMM-N) como almacenamiento Byte-Addressable en Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Para ayudar a los desarrolladores a aprovechar las ventajas de las ofertas de memoria persistentes, Microsoft también ha contribuido a la realización de la biblioteca de memoria no volátil (NVML) en Windows. Esta biblioteca proporciona varias herramientas para hacer que las aplicaciones reconozcan la memoria de forma persistente. Por ejemplo, contiene código que le permite crear fácilmente un almacén de clave-valor para PM para búsquedas y almacenes extremadamente rápidos. Puede encontrar más información sobre NVML, incluidos ejemplos, en la [biblioteca NVM](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integración de NVML en un proyecto de Visual Studio

1. Descargar archivos y encabezados de la biblioteca NVML

-   NVML se mantiene en GitHub. Puede compilar el origen usted mismo o simplemente descargar los archivos binarios compilados directamente desde aquí: [NVML versión 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Coloque los archivos de biblioteca y los encabezados en un directorio de su elección, por ejemplo: "C: \\ NVML \\ lib" y "c: \\ NVML \\ Inc", respectivamente.

3. Configure el proyecto de la siguiente manera:

-   Abra el proyecto de Visual Studio y, en el "Explorador de soluciones", haga clic con el botón derecho en el nombre del proyecto.
-   Abra el panel de configuración del proyecto en la parte inferior del elemento emergente resultante.
-   Vaya a "propiedades de configuración-> C/C++" y agregue la carpeta en la que ha almacenado el encabezado (C: \\ NVML \\ Inc) al campo "directorios de inclusión adicionales".
-   A continuación, vaya a "propiedades de configuración-> vinculador" y agregue la carpeta en la que ha almacenado la biblioteca (C: \\ NVML \\ lib) al campo "directorios de biblioteca adicionales".

4. Después, asegúrese de que tiene como destino el proyecto para Windows Server 2016 o la actualización de aniversario de Windows 10:

-   Vaya a "propiedades de configuración-> general" y establezca el campo "versión de la plataforma de destino" en "10.0.14393.0" y
-   Vaya a "propiedades de configuración-> C/C++" y agregue "NTDDI \_ version = NTDDI \_ WIN10 \_ RS1;" al campo "preprocesador".

5. Incluya los encabezados en el código y vincúlelo a las bibliotecas necesarias.

-   En este momento, puede incluir simplemente los archivos de encabezado que desea usar en el código como cualquier otro archivo de encabezado. Por ejemplo, para usar libpmem:
    -   Agregue " \# include <libpmem. h>" y
    -   Agregue "libpmem. lib" a "propiedades de configuración-> enlazador-> INPUT-> dependencias adicionales"

En este momento, está listo para llamar directamente a las funciones de la biblioteca en el código y aprovecharlas.

 

 



