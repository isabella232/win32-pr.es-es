---
title: Distribución de la multisesión de IMAPi
description: IMAPi proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en CD, DVD y Blu-Ray \ 8482; medios ópticos.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104566311"
---
# <a name="imapi-multisession-layout"></a>Distribución de la multisesión de IMAPi

IMAPi proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en medios ópticos de CD, DVD y Blu-Ray™. Con Windows 7, IMAPi proporciona compatibilidad adicional para la grabación de múltiples sesiones en DVD y Blu-Ray™ medios regrabables.

La siguiente documentación detalla el diseño del disco que IMAPi emplea para implementar la multisesión. Esta información debe usarse para garantizar la interoperabilidad entre IMAPi y otro software de grabación, además de permitir que los desarrolladores de este software creen imágenes de disco de múltiples sesiones compatibles con IMAPi.

> [!Note]  
> Para ver un ejemplo en el que se detalla la creación de un disco de múltiples sesiones, consulte [creación de un disco de múltiples sesiones](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Multisesión en medios secuenciales

La implementación de IMAPi de multisesión en medios secuenciales se admite para su uso con los medios CD-R, CD-RW, DVD-R, DVD + R y Blu-Ray™. IMAPi usa el modo de grabación de sesión a la vez para CD-RW y, como resultado, en este escenario, el formato se considera un tipo de medio secuencial.

En un escenario en el que se usa la multisesión en medios secuenciales con UDF, IMAPi escribe las estructuras de delimitador (delimitador de volumen del delimitador UDF-AVDP), las estructuras de volumen (UDF del descriptor de volumen de UDF) y las estructuras de metadatos del sistema de archivos (archivo UDF Set descriptor-FSD) al principio de

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el punto de montaje ' Import/F S ' indicado con una flecha roja en el ' delimitador ' de la sesión física 2.](images/multises1.png)

> [!Note]  
> En esta ilustración se muestra el diseño del disco IMAPi cuando se usa la UDF 2,50 con metadatos redundantes.

 

Los datos almacenados en medios grabados secuencialmente se componen de varias sesiones físicas. Cada sesión contiene un sistema de archivos completo que representa los datos de usuario como un conjunto de archivos organizados en directorios. Los metadatos del sistema de archivos se componen de varias estructuras de datos organizadas jerárquicamente. En la parte superior de la jerarquía, se encuentran las estructuras de delimitador (AVDP) ubicadas en direcciones de bloques lógicos predefinidas (LBAs). Las estructuras de delimitador especifican las ubicaciones de las siguientes estructuras de nivel que no tienen direcciones predefinidas. El siguiente nivel de jerarquía después de las estructuras de delimitador contiene las estructuras de volumen (VDS) que describen las propiedades del volumen y hacen referencia a las estructuras de metadatos del sistema de archivos (FSD), que a su vez describen archivos y directorios individuales.

## <a name="multisession-on-rewritable-media"></a>Multisesión en medios regrabables

El enfoque para los medios secuenciales descritos en la sección anterior es incompatible con los medios regrabables (no secuenciales). Estos formatos de medios incluyen DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ reescribible y otros medios de escritura aleatorios, como discos de REV Iomega. Los medios regrabables no admiten el concepto de sesiones físicas correspondientes a las sesiones lógicas, que son incrementos individuales confirmados por una aplicación de maestro. Solo se expone una única sesión física, que es un área que empieza al principio del disco que representa el área completa que tiene la posibilidad de contener varias sesiones lógicas.

> [!Note]  
> Aunque DVD-RW es una excepción en que admite el concepto de una sesión física en el modo secuencial, esta funcionalidad no es compatible actualmente con IMAPi.

 

Para solucionar la falta de una asignación de uno a uno entre sesiones físicas y lógicas en formatos regrabables, IMAPi actualiza selectivamente las estructuras de delimitador (AVDP) en la *primera* sesión lógica para apuntar a las nuevas estructuras de volumen (VDS) y a las estructuras de metadatos del sistema de archivos (FSD) al principio de la *última* sesión lógica, como se describe en

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el punto de montaje ' Import/F S ' indicado con una flecha roja en el ' delimitador ' de la sesión lógica 1.](images/multises2.png)

> [!Note]  
> En esta ilustración se muestra el diseño del disco IMAPi cuando se usa la UDF 2,50 con metadatos redundantes.

 

Al agregar una nueva sesión lógica a un disco regrabable, IMAPi primero determina el final de la última sesión lógica mediante el análisis de los metadatos del volumen (VDS). A continuación, IMAPi agrega la nueva sesión lógica, completa con las nuevas estructuras de delimitador (AVDP), volumen (VDS) y de metadatos del sistema de archivos (FSD), contiguas físicamente con la sesión lógica registrada previamente. El último paso requiere que se actualicen las estructuras de delimitador (AVDP) al principio de la primera sesión lógica para que apunten a las estructuras de volumen (VDS) en la *nueva* sesión lógica. El resultado operativo es el mismo que con los medios secuenciales.

## <a name="additional-recommendations"></a>Recomendaciones adicionales

-   **Diseño de partición**

    Para lograr la compatibilidad con IMAPi, se recomienda que los desarrolladores de software de grabación de terceros usen los diseños de disco descritos en esta documentación. Los desarrolladores deben evitar los diseños con particiones del sistema de archivos que ocupen todo el disco, ya que esto requiere la grabación de las aplicaciones para localizar espacio disponible en las particiones existentes siempre que sea necesario anexar datos al disco. A menudo, las aplicaciones de grabación logran esto mediante el uso de marcadores propietarios en el disco para indicar cuánto espacio ocupa realmente los datos de usuario. Estos diseños de disco son incompatibles con IMAPi, ya que los marcadores propietarios no se reconocen fuera de la aplicación para la que se crearon.

-   **Tipo de partición UDF**

    IMAPi usa el tipo de partición UDF de **solo lectura** en su implementación de multisesión en medios regrabables. Los desarrolladores de software de grabación de terceros deben usar el tipo de partición UDF de **solo lectura** para lograr la compatibilidad con la grabación con registro maestro de Windows a través de IMAPI. Si se usa otro tipo de partición UDF, como **reescritura** , IMAPI no puede proporcionar compatibilidad con la creación de patrones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un disco de múltiples sesiones](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




