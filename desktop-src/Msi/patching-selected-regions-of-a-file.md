---
description: Al aplicar revisiones a los archivos que tienen contenido variable, puede que sea necesario conservar las regiones seleccionadas del archivo de destino para evitar la pérdida de información crítica.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Aplicar revisiones a las regiones seleccionadas de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c075a3632dd6cf4d39a98467503c584cbf34a15311f37d0c8aabe0990bc74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926244"
---
# <a name="patching-selected-regions-of-a-file"></a>Aplicar revisiones a las regiones seleccionadas de un archivo

Al aplicar revisiones a los archivos que tienen contenido variable, puede que sea necesario conservar las regiones seleccionadas del archivo de destino para evitar la pérdida de información crítica. Por ejemplo, algunas aplicaciones marcan la información del usuario en el archivo ejecutable. Dado que el contenido del archivo de destino puede depender del equipo en el que está instalada la aplicación, resulta difícil determinar si un archivo determinado es un destino válido para la revisión. La información de usuario escrita en el archivo de destino también se puede sobrescribir mediante una revisión.

Al generar un archivo de propiedades de creación de revisiones (PATCH) con [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md), puede especificar que la información de determinadas regiones del archivo de destino se ignore durante la aplicación de revisiones. También puede especificar que la información de otras regiones del archivo de destino se conserve y copie en una ubicación de desplazamiento del archivo actualizado. Especifique las regiones del archivo de destino que se omitirán y las regiones que se conservarán al crear las tablas OptionalData, [ExternalFiles](externalfiles-table-patchwiz-dll-.md)y [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) de [TargetFiles.](targetfiles-optionaldata-table-patchwiz-dll-.md)

Use la columna RetainOffsets de la tabla [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) y las columnas RetainOffsets y RetainLengths de la tabla [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) para copiar un intervalo de información del archivo de destino en un intervalo de desplazamiento del archivo actualizado. Se conserva la información de este intervalo. Especifique la longitud del intervalo mediante las columnas RetainLengths de la tabla FamilyFileRanges. La longitud del intervalo retenido es la misma en los archivos de destino y actualizados. Especifique el desplazamiento del intervalo en el archivo de destino mediante la columna RetainOffsets de la tabla TargetFiles OptionalData. Especifique el desplazamiento del intervalo en el archivo actualizado mediante la columna RetainOffsets de la tabla FamilyFileRanges. Por lo tanto, el intervalo del archivo de destino retenido es el valor de RetainOffsets en la tabla OptionalData de TargetFiles más RetainLengths. Esta información se copia en el archivo de actualización en el intervalo especificado por el valor de RetainOffsets en las tablas FamilyFileRanges más RetainLengths. Puede especificar varios intervalos, pero el orden de las longitudes debe coincidir con el orden de los desplazamientos.

Use la [tabla OptionalData de TargetFiles](targetfiles-optionaldata-table-patchwiz-dll-.md) para omitir un intervalo del archivo de destino. La revisión todavía puede sobrescribir la información de este intervalo del archivo de destino. Especifique el desplazamiento del intervalo en la columna IgnoreOffsets y su longitud en la columna IgnoreLengths. Puede especificar varios intervalos, pero el orden de las longitudes debe coincidir con el orden de los desplazamientos.

Los valores de las columnas lengths y offsets pueden ser decimales o hexadecimales. [PATCHWIZ.DLL](patchwiz-dll.md) trata el valor como hexadecimal si tiene el prefijo "0x". Las columnas son columnas de cadena, por lo PATCHWIZ.DLL convierte los valores en ULONG. La columna length especifica la longitud en bytes.

 

 



