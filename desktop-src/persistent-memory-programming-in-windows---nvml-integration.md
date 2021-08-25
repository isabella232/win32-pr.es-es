---
description: La tecnología de memoria persistente (PM) proporciona acceso de nivel de byte a medios no volátiles, a la vez que reduce considerablemente la latencia de almacenamiento o recuperación de datos.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programación de memoria persistente en Windows integración de NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750a05f28ca4698091f79b1004bbbb00ff69752e0ff45f2153cc4f0b7fe20a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951055"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programación de memoria persistente en Windows integración de NVML

La tecnología de memoria persistente (PM) proporciona acceso de nivel de byte a medios no volátiles, a la vez que reduce considerablemente la latencia de almacenamiento o recuperación de datos. Crea un nuevo nivel entre la memoria de un sistema y el almacenamiento tradicional. Cualquier programa que dependa de o se escale con escrituras rápidas en un medio persistente puede beneficiarse de pm.

El propósito de este artículo es describir cómo se puede integrar la biblioteca de memoria no volátil (NVML) en un proyecto Visual Studio para facilitar su uso.

> [!Note]  
> La memoria persistente a veces también se conoce como Storage de clase persistente (SCM).

 

## <a name="pm-and-nvml"></a>PM y NVML

La primera compatibilidad con la memoria persistente se introdujo en Windows Server 2016 y la actualización Windows 10 aniversario (1607). Para obtener información general rápida, consulte estos dos vídeos de Channel9:

-   [Uso de memoria no volátil (NVDIMM-N) como almacenamiento en bloques en Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Uso de memoria no volátil (NVDIMM N) como almacenamiento direccionable por bytes en Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Para ayudar a los desarrolladores a aprovechar las ventajas que ofrece la memoria persistente, Microsoft también ha contribuido a los esfuerzos de llevar la biblioteca de memoria no volátil (NVML) a Windows. Esta biblioteca proporciona varias herramientas para que las aplicaciones conozcan la memoria persistente. Por ejemplo, contiene código que le permite crear fácilmente un almacén de clave-valor con conocimiento de PM para almacenes y busca-ups extremadamente rápidos. Puede encontrar más información sobre NVML, incluidos ejemplos, en [biblioteca nvm](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integración de NVML en un Visual Studio Project

1. Descarga de encabezados y archivos de biblioteca NVML

-   NVML se mantiene en GitHub. Puede compilar el origen usted mismo o simplemente descargar archivos binarios compilados directamente desde aquí: [NVML versión 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Coloque los archivos de biblioteca y los encabezados en un directorio de su elección, por ejemplo: "C: \\ biblioteca NVML" y \\ "C: \\ NVML \\ inc", respectivamente.

3. Configure el proyecto de la siguiente manera:

-   Abra el proyecto de Visual Studio y, en "Explorador de soluciones", haga clic con el botón derecho en el nombre del proyecto.
-   Abra el panel de configuración del proyecto en la parte inferior del menú emergente resultante.
-   Vaya a "Propiedades de configuración -> C/C++" y agregue la carpeta en la que ha almacenado el encabezado (C: NVML inc) al campo "Directorios de incluir \\ \\ adicionales".
-   A continuación, vaya a "Propiedades de configuración -> Linker" y agregue la carpeta en la que ha almacenado la biblioteca (C: biblioteca NVML) al campo "Directorios de biblioteca \\ \\ adicionales".

4. A continuación, asegúrese de que tiene como destino el proyecto para Windows Server 2016 o Windows 10 de aniversario:

-   Vaya a "Propiedades de configuración -> General" y establezca el campo "Versión de la plataforma de destino" en "10.0.14393.0" y
-   Vaya a "Propiedades de configuración -> C/C++" y agregue "NTDDI \_ VERSION=NTDDI \_ WIN10 \_ RS1;" al campo "Preprocesador".

5. Incluir los encabezados en el código y vincular a las bibliotecas necesarias

-   En este momento, puede incluir simplemente los archivos de encabezado que quiere usar en el código como cualquier otro archivo de encabezado. Por ejemplo, para usar libpmem:
    -   add " \# include <libpmem.h>" y
    -   agregue "libpmem.lib" a "Propiedades de configuración -> Linker -> Input -> Dependencias adicionales"

En este momento, está listo para llamar a las funciones de la biblioteca directamente en el código y aprovecharlas.

 

 



