---
description: Al aplicar una revisión a los archivos que tienen contenido variable, puede ser necesario conservar las regiones seleccionadas del archivo de destino para evitar la pérdida de información crítica.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Aplicar revisiones a las regiones seleccionadas de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778df4b0cc98eeacd1106929b18c7461c6fa9e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652503"
---
# <a name="patching-selected-regions-of-a-file"></a>Aplicar revisiones a las regiones seleccionadas de un archivo

Al aplicar una revisión a los archivos que tienen contenido variable, puede ser necesario conservar las regiones seleccionadas del archivo de destino para evitar la pérdida de información crítica. Por ejemplo, algunas aplicaciones marcan información de usuario en el archivo ejecutable. Dado que el contenido del archivo de destino puede depender del equipo en el que está instalada la aplicación, resulta difícil determinar si un archivo determinado es un destino válido para la revisión. La información de usuario escrita en el archivo de destino también se puede sobrescribir con una revisión.

Al generar un archivo de propiedades de creación de revisiones (PCP) con [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md), puede especificar que se omita la información de ciertas regiones del archivo de destino durante la revisión. También puede especificar que la información de otras regiones del archivo de destino se retenga y copie en una ubicación de desplazamiento en el archivo actualizado. Especifique qué regiones del archivo de destino se omitirán y qué regiones se conservarán al crear las tablas [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md), [ExternalFiles](externalfiles-table-patchwiz-dll-.md)y [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) .

Use la columna RetainOffsets de la tabla [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) y las columnas RetainOffsets y RetainLengths de la tabla [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) para copiar un intervalo de información del archivo de destino en un intervalo de desplazamiento en el archivo actualizado. Se conserva la información de este intervalo. Especifique la longitud del intervalo mediante las columnas RetainLengths de la tabla FamilyFileRanges. La longitud del intervalo retenido es la misma en los archivos de destino y actualizados. Especifique el desplazamiento del intervalo en el archivo de destino mediante la columna RetainOffsets de la tabla OptionalData de TargetFiles. Especifique el desplazamiento del intervalo en el archivo actualizado mediante la columna RetainOffsets de la tabla FamilyFileRanges. El intervalo del archivo de destino retenido es, por lo tanto, el valor de RetainOffsets en la tabla TargetFiles OptionalData y RetainLengths. Esta información se copia en el archivo de actualización en el intervalo proporcionado por el valor de RetainOffsets en las tablas FamilyFileRanges más RetainLengths. Puede especificar varios intervalos, pero el orden de las longitudes debe coincidir con el orden de los desplazamientos.

Use la tabla [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) para omitir un intervalo del archivo de destino. La revisión puede seguir sobrescribiendo la información de este intervalo del archivo de destino. Especifique el desplazamiento del intervalo en la columna IgnoreOffsets y su longitud en la columna IgnoreLengths. Puede especificar varios intervalos, pero el orden de las longitudes debe coincidir con el orden de los desplazamientos.

Los valores de las columnas longitudes y desplazamientos pueden ser decimales o hexadecimales. [PATCHWIZ.DLL](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena, por lo que PATCHWIZ.DLL convierte los valores en ULONGs. La columna longitud especifica la longitud en bytes.

 

 



