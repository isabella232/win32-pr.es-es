---
title: Diseño de varias sesiones de IMAPI
description: IMAPI proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en CD, DVD y Blu-Ray \ 8482; medios ópticos.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d816d293a3474f46dc3a48577a46615672103099dc2aa561d393953f29ccf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249421"
---
# <a name="imapi-multisession-layout"></a>Diseño de varias sesiones de IMAPI

IMAPI proporciona a los desarrolladores de aplicaciones la capacidad de crear imágenes del sistema de archivos ISO 9660 y UDF y grabarlas en CD, DVD y Dv-Ray™ medios ópticos. Con Windows 7, IMAPI proporciona compatibilidad adicional para la grabación multisesión en DVD ™ medios que se pueden volver a escribir.

En la siguiente documentación se detalla el diseño del disco que IMAPI usa para implementar la multisesión. Esta información debe usarse para garantizar la interoperabilidad entre IMAPI y otro software de grabación, así como para permitir a los desarrolladores de este software crear imágenes de disco multisesión compatibles con IMAPI.

> [!Note]  
> Para obtener un ejemplo en el que se detalla la creación de un disco de varias sesiones, vea [Creating a Multisession Disc](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Multisesión en medios secuenciales

La implementación DE IMAPI de multisesión en medios secuenciales se admite para su uso con cd-R, CD-RW, DVD-R, DVD+R ™ multimedia. IMAPI usa el modo de grabación session-at-once para CD-RW y, como resultado, en este escenario, el formato se considera un tipo de medio secuencial.

En un escenario que implica varias sesiones en medios secuenciales mediante UDF, IMAPI escribe las estructuras delimitadoras (UDF Anchor Volume Descriptor Pointer - AVDP), las estructuras de volumen (UDF Volume Descriptor Sequence - VDS) y las estructuras de metadatos del sistema de archivos (UDF File Set Descriptor - FSD) al principio de cada nueva sesión, como se describe en el diagrama siguiente:

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el "punto de montaje import/F S" indicado con una flecha roja en el "Delimitador" de la sesión física 2.](images/multises1.png)

> [!Note]  
> En esta ilustración se muestra el diseño del disco IMAPI cuando se usa UDF 2.50 con metadatos redundantes.

 

Los datos almacenados en medios registrados secuencialmente constan de varias sesiones físicas. Cada sesión contiene un sistema de archivos completo que representa los datos de usuario como un conjunto de archivos organizados en directorios. Los metadatos del sistema de archivos constan de varias estructuras de datos organizadas jerárquicamente. En la parte superior de la jerarquía residen estructuras delimitadoras (AVDP) ubicadas en direcciones de bloque lógico (LBA) predefinidas. Las estructuras delimitadoras especifican las ubicaciones de las estructuras de nivel siguiente que no tienen direcciones predefinidas. El siguiente nivel de jerarquía después de las estructuras delimitadoras contiene las estructuras de volumen (VDS) que describen las propiedades del volumen y hacen referencia a las estructuras de metadatos del sistema de archivos (FSD), que a su vez describen archivos y directorios individuales.

## <a name="multisession-on-rewritable-media"></a>Multisesión en medios reescritos

El enfoque de los medios secuenciales descritos en la sección anterior no es compatible con los medios que se pueden volver a escribir (no secuenciales). Estos formatos multimedia incluyen DVD-RW, DVD+RW, DVD-RAM™ reescritable y otros medios de escritura aleatorios, como discos iomega REV. Los medios reescritos no admiten el concepto de sesiones físicas correspondientes a sesiones lógicas, que son incrementos individuales confirmados por una aplicación de mastering. Solo se expone una sesión física, que es un área que comienza al principio del disco y que representa todo el área direccionable que puede contener varias sesiones lógicas.

> [!Note]  
> Aunque DVD-RW es una excepción en el sentido de que admite el concepto de sesión física en el modo secuencial, esta funcionalidad no es compatible actualmente con IMAPI.

 

Para solucionar la falta de asignación uno a uno entre sesiones físicas y lógicas en formatos que  se pueden volver a escribir, IMAPI actualiza selectivamente las estructuras delimitadoras (AVDP) de la primera sesión lógica para que apunten a las nuevas estructuras de volumen (VDS) y a las estructuras de metadatos del sistema de archivos (FSD) al principio de la última sesión lógica, tal como se describe en el diagrama siguiente: 

![Diagrama que muestra la estructura de metadatos del sistema de archivos con el punto de montaje "Import/F S" indicado con una flecha roja en el "Delimitador" de la sesión lógica 1.](images/multises2.png)

> [!Note]  
> En esta ilustración se muestra el diseño del disco IMAPI cuando se usa UDF 2.50 con metadatos redundantes.

 

Al agregar una nueva sesión lógica a un disco que se puede volver a escribir, IMAPI determina primero el final de la última sesión lógica mediante el análisis de los metadatos del volumen (VDS). A continuación, IMAPI agrega la nueva sesión lógica, completa con nuevas estructuras de anclaje (AVDP), volumen (VDS) y metadatos del sistema de archivos (FSD), físicamente contiguas con la sesión lógica registrada anteriormente. El paso final requiere que las estructuras delimitadoras (AVDP) al principio de la primera sesión lógica se actualicen para que apunten a las estructuras de volumen (VDS) de la *nueva* sesión lógica. El resultado operativo es el mismo que con los medios secuenciales.

## <a name="additional-recommendations"></a>Recomendaciones adicionales

-   **Diseño de partición**

    Para lograr la compatibilidad con IMAPI, se recomienda que los desarrolladores de software de grabación de terceros usen los diseños de disco que se describen en esta documentación. Los desarrolladores deben evitar los diseños con particiones del sistema de archivos que ocupan todo el disco, ya que esto requiere que las aplicaciones de grabación busquen espacio libre en las particiones existentes siempre que sea necesario anexar datos al disco. A menudo, las aplicaciones de grabación lo logran mediante el uso de marcadores propietarios en el disco para indicar la cantidad de espacio ocupado realmente por los datos del usuario. Estos diseños de disco no son compatibles con IMAPI, ya que los marcadores propietarios no se reconocen fuera de la aplicación para la que se crearon.

-   **Tipo de partición UDF**

    IMAPI usa el **tipo de partición** UDF de solo lectura en su implementación de multisesión en medios que se pueden volver a escribir. Los desarrolladores de software de grabación de terceros deben usar el tipo de partición **UDF** de solo lectura para lograr la compatibilidad con Windows a través de IMAPI. Si se usa otro tipo de partición UDF como **Rewritable,** IMAPI no puede proporcionar compatibilidad con la mastering.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un disco multisesión](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




