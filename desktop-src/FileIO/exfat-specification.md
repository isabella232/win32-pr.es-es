---
description: Especificación del sistema de archivos exComp.
title: Especificación del sistema de archivos exDESC
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 94b5bcdc69201573bc92290c148a7d3ce8304868
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119020"
---
# <a name="exfat-file-system-specification"></a>Especificación del sistema de archivos exDESC

## <a name="1-introduction"></a>1 Introducción

El sistema de archivos ex FAT es el sucesor de FAT32 en la familia FAT de sistemas de archivos. Esta especificación describe el sistema de archivos exDORES y proporciona toda la información necesaria para implementar el sistema de archivos ex UNO.

### <a name="11-design-goals"></a>1.1 Objetivos de diseño

El sistema de archivos ex UNO tiene tres objetivos de diseño centrales (consulte la lista siguiente).

1. *Conserve la simplicidad de los sistemas de archivos basados en FAT.*

   > Dos de los puntos fuertes de los sistemas de archivos basados en FAT son su simplicidad relativa y facilidad de implementación. En el pasado de sus predecesores, a los implementadores le resultaba relativamente sencillo y fácil de implementar.

2. *Habilite archivos y dispositivos de almacenamiento muy grandes.*

   > El sistema de archivos ex PROP usa 64 bits para describir el tamaño de archivo, lo que permite aplicaciones que dependen de archivos muy grandes. El sistema de archivos ex USB también permite clústeres de hasta 32 MB, lo que permite de forma eficaz dispositivos de almacenamiento muy grandes.

3. *Incorpore extensibilidad para la innovación futura.*

   > El sistema de archivos ex USB incorpora extensibilidad en su diseño, lo que permite que el sistema de archivos siga el ritmo de las innovaciones en el almacenamiento y los cambios en el uso.

### <a name="12-specific-terminology"></a>1.2 Terminología específica

En el contexto de esta especificación, ciertos términos (consulte la tabla [1)](#table-1-definition-of-terms-which-carry-very-specific-meaning)tienen un significado específico para el diseño y la implementación del sistema de archivos ex UNO.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Definición de tabla 1 de términos que tienen un significado muy específico**

<table>
<thead>
<tr class="header">
<th><strong>Término</strong></th>
<th><strong>Definición</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Debe</td>
<td>Esta especificación usa el término "shall" para describir un comportamiento que es obligatorio.</td>
</tr>
<tr class="even">
<td>Posible</td>
<td>Esta especificación usa el término "should" para describir un comportamiento que recomienda encarecidamente, pero no hace obligatorio.</td>
</tr>
<tr class="odd">
<td>May</td>
<td>Esta especificación usa el término "may" para describir un comportamiento que es opcional.</td>
</tr>
<tr class="even">
<td>Mandatory</td>
<td>Este término describe un campo o estructura que una implementación debe modificar y debe interpretar como se describe en esta especificación.</td>
</tr>
<tr class="odd">
<td>Opcional</td>
<td>Este término describe un campo o estructura que una implementación puede admitir o no. Si una implementación admite un campo o una estructura opcional determinados, modificará e interpretará el campo o la estructura como se describe en esta especificación.</td>
</tr>
<tr class="even">
<td>No definido</td>
<td>Este término describe el contenido de campo o estructura que una implementación puede modificar según sea necesario (es decir, borrar a cero al establecer campos o estructuras circundantes) y no debe interpretar para contener ningún significado específico.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td><p>En este término se describe el contenido del campo o la estructura que las implementaciones:</p>
<ol type="1">
<li><p>Debe inicializarse en cero y no debe usarse para ningún propósito.</p></li>
<li><p>No debe interpretarse, excepto cuando se computan sumas de comprobación</p></li>
<li><p>Debe conservar entre las operaciones que modifican los campos o estructuras circundantes.</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1.3 Texto completo de acrónimos comunes

Esta especificación usa acrónimos en uso común en el sector de los equipos personales (consulte [la tabla 2).](#table-2-full-text-of-common-acronyms)

<div id="table-2-full-text-of-common-acronyms" />

**Texto completo de la tabla 2 de acrónimos comunes**

| **Acrónimo** | **Texto completo**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Sistema de salida de entrada básico                          |
| CPU         | Unidad de procesamiento central                            |
| exFAT       | tabla extensible de asignación de archivos                   |
| FAT         | Tabla de asignación de archivos                              |
| FAT12       | Tabla de asignación de archivos, índices de clúster de 12 bits      |
| FAT16       | Tabla de asignación de archivos, índices de clúster de 16 bits      |
| FAT32       | Tabla de asignación de archivos, índices de clúster de 32 bits      |
| GPT         | tabla de particiones GUID                               |
| GUID        | Identificador único global (consulte [la sección 10.1)](#101-globally-unique-identifiers-guids)      |
| INT         | Interrupción                                          |
| MBR         | registro de arranque maestro                                 |
| traslación      | ExCOMP segura para transacciones                             |
| UTC         | Hora universal coordinada                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1.4 Calificadores predeterminados de campo y estructura

Los campos y estructuras de esta especificación tienen los siguientes calificadores (consulte la lista siguiente), a menos que la especificación indique lo contrario.

1. Sin signo

2. Use la notación decimal para describir valores, donde no se indique lo contrario; esta especificación usa la letra posterior a la corrección "h" para indicar números hexadecimales y incluye GUID entre llaves.

3. Están en formato little-endian

4. No se requiere un carácter de terminación null para las cadenas

### <a name="15-windows-ce-and-texfat"></a>1.5 Windows CE y Texas QUE

Tex ZOOM es una extensión de ex SUF que agrega semántica operativa segura para transacciones sobre el sistema de archivos base. La utiliza el Windows CE.
Para usar en transacciones, Se requiere el uso de los dos mapas de bits de asignación y las dos FAT. También define varias estructuras adicionales, incluidos descriptores de relleno y descriptores de seguridad.

## <a name="2-volume-structure"></a>2 Estructura del volumen

Un volumen es el conjunto de todas las estructuras del sistema de archivos y el espacio de datos necesarios para almacenar y recuperar datos de usuario. Todos los volúmenes ex RAID contienen cuatro regiones (consulte [la tabla 3).](#table-3-volume-structure)

<div id="table-3-volume-structure" />

**Estructura de volúmenes de tabla 3**

<table>
<thead>
<tr class="header">
<th><strong>Nombre de la subr region</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(sector)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(sectores)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Región de arranque principal</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Sector de arranque principal</td>
<td>0</td>
<td>1</td>
<td>Esta subrrea es obligatoria y <a href="#31-main-and-backup-boot-sector-sub-regions">la sección 3.1</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Principales sectores de arranque extendido</td>
<td>1</td>
<td>8</td>
<td>Esta subr region es obligatoria y <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">la sección 3.2</a>) define su contenido.</td>
</tr>
<tr class="even">
<td>Parámetros principales de OEM</td>
<td>9</td>
<td>1</td>
<td>Esta región es obligatoria y <a href="#33-main-and-backup-oem-parameters-sub-regions">la sección 3.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado principal</td>
<td>10</td>
<td>1</td>
<td>Esta subr region es obligatoria y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>Suma de comprobación de arranque principal</td>
<td>11</td>
<td>1</td>
<td>Esta subr region es obligatoria y <a href="#34-main-and-backup-boot-checksum-sub-regions">la sección 3.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td><strong>Región de arranque de copia de seguridad</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Sector de arranque de copia de seguridad</td>
<td>12</td>
<td>1</td>
<td>Esta subr region es obligatoria y <a href="#31-main-and-backup-boot-sector-sub-regions">la sección 3.1</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Copia de seguridad de sectores de arranque extendido</td>
<td>13</td>
<td>8</td>
<td>Esta subr region es obligatoria y <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">la sección 3.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Parámetros de OEM de copia de seguridad</td>
<td>21</td>
<td>1</td>
<td>Esta región es obligatoria y <a href="#33-main-and-backup-oem-parameters-sub-regions">la sección 3.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Copia de seguridad reservada</td>
<td>22</td>
<td>1</td>
<td>Esta subr region es obligatoria y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>Suma de comprobación de arranque de copia de seguridad</td>
<td>23</td>
<td>1</td>
<td>Esta subr region es obligatoria y <a href="#34-main-and-backup-boot-checksum-sub-regions">la sección 3.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td><strong>Región FAT</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alineación de FAT</td>
<td>24</td>
<td>FatOffset: 24</td>
<td><p>Esta subr region es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo FatOffset.</p></td>
</tr>
<tr class="odd">
<td>First FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Esta subr region es obligatoria y <a href="#41-first-and-second-fat-sub-regions">la sección 4.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset y FatLength.</p></td>
</tr>
<tr class="even">
<td>Segundo FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOf Fats – 1)</td>
<td><p>Esta subr region es obligatoria y <a href="#41-first-and-second-fat-sub-regions">la sección 4.1</a> define su contenido, si existe.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset, FatLength y NumberOfAturas. El campo NumberOfFats solo puede contener los valores 1 y 2.</p></td>
</tr>
<tr class="odd">
<td><strong>Región de datos</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alineación del montón de clúster</td>
<td>FatOffset + FatLength * NumberOf Fats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOf Daxs)</td>
<td><p>Esta subr region es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset, FatLength, NumberOf Fats y ClusterHeapOffset. Los valores válidos del campo NumberOfPlants son 1 y 2.</p></td>
</tr>
<tr class="odd">
<td>Montón de clúster</td>
<td>ClusterHeapOffset</td>
<td>ClusterCount * 2<sup>SectoresPerClusterShift</sup></td>
<td><p>Esta subr region es obligatoria y <a href="#51-cluster-heap-sub-region">la sección 5.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset, ClusterCount y SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Espacio excesivo</td>
<td>ClusterHeapOffset + ClusterCount * 2<sup>SectoresPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + ClusterCount * 2<sup>SectoresPerClusterShift</sup>)</td>
<td><p>Esta subr region es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset, ClusterCount, SectorsPerClusterShift y VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 regiones principales y de arranque de copia de seguridad

La región de arranque principal proporciona todas las instrucciones necesarias para el arranque, la información de identificación y los parámetros del sistema de archivos para permitir que una implementación realice lo siguiente:

1. Arranque y arranque un sistema informático desde un volumen ex RAID.

2. Identifique el sistema de archivos del volumen como ex RAID.

3. Descubra la ubicación de las estructuras del sistema de archivos exSTRUCCIONES.

La región de arranque de copia de seguridad es una copia de seguridad de la región de arranque principal. Ayuda a la recuperación del volumen ex RAID en caso de que la región de arranque principal esté en un estado incoherente. Excepto en circunstancias poco frecuentes, como la actualización de instrucciones de arranque, las implementaciones no deben modificar el contenido de la región de arranque de copia de seguridad.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3.1 Subrecciones del sector principal y de arranque de copia de seguridad

El sector de arranque principal contiene código para el arranque a partir de un volumen ex RAID y parámetros fundamentales de ex RAID que describen la estructura del volumen (vea [la tabla 4).](#table-4-main-and-backup-boot-sector-structure) BIOS, MBR u otros agentes de arranque pueden inspeccionar este sector y pueden cargar y ejecutar las instrucciones de arranque contenidas en este.

El sector de arranque de copia de seguridad es una copia de seguridad del sector de arranque principal y tiene la misma estructura (consulte [la tabla 4).](#table-4-main-and-backup-boot-sector-structure) El sector de arranque de copia de seguridad puede ayudar a las operaciones de recuperación. Sin embargo, las implementaciones deben tratar el contenido de los campos VolumeFlags y PercentInUse como obsoleto.

Antes de usar el contenido del sector de arranque principal o de copia de seguridad, las implementaciones deben comprobar su contenido validando su respectiva suma de comprobación de arranque y asegurándose de que todos sus campos están dentro de su intervalo de valores válido.

Aunque la operación de formato inicial inicializará el contenido de los sectores principal y de arranque de copia de seguridad, las implementaciones pueden actualizar estos sectores (y también actualizar sus respectivas sumas de comprobación de arranque) según sea necesario. Sin embargo, las implementaciones pueden actualizar los campos VolumeFlags o PercentInUse sin actualizar su respectiva suma de comprobación de arranque (la suma de comprobación excluye específicamente estos dos campos).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabla 4 Estructura del sector principal y de arranque de copia de seguridad**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Este campo es obligatorio y <a href="#311-jumpboot-field">la sección 3.1.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#312-filesystemname-field">la sección 3.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Este campo es obligatorio y <a href="#313-mustbezero-field">la sección 3.1.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#314-partitionoffset-field">la sección 3.1.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#315-volumelength-field">la sección 3.1.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#316-fatoffset-field">la sección 3.1.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#317-fatlength-field">la sección 3.1.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#318-clusterheapoffset-field">la sección 3.1.8</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>ClusterCount</td>
<td>92</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#319-clustercount-field">la sección 3.1.9</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3110-firstclusterofrootdirectory-field">la sección 3.1.10</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3111-volumeserialnumber-field">la sección 3.1.11</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#3112-filesystemrevision-field">la sección 3.1.12</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#3113-volumeflags-field">la sección 3.1.13</a> define su contenido.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#3114-bytespersectorshift-field">la sección 3.1.14</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#3115-sectorsperclustershift-field">la sección 3.1.15</a> define su contenido.</td>
</tr>
<tr class="even">
<td>NumberOfPlants</td>
<td>110</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#3116-numberoffats-field">la sección 3.1.16</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#3117-driveselect-field">la sección 3.1.17</a> define su contenido.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#3118-percentinuse-field">la sección 3.1.18</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>113</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>BootCode</td>
<td>120</td>
<td>390</td>
<td>Este campo es obligatorio y <a href="#3119-bootcode-field">la sección 3.1.19</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#3120-bootsignature-field">la sección 3.1.20</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>bytesPerSectorShift</sup> – 512</td>
<td><p>Este campo es obligatorio y su contenido, si existe, no está definido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot Field

El campo JumpBoot debe contener la instrucción de salto para las CPU comunes en equipos personales que, cuando se ejecutan, "salta" la CPU para ejecutar las instrucciones de arranque en el campo BootCode.

El valor válido para este campo es (en orden de byte de orden bajo a byte de orden superior) EBh 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 Campo FileSystemName

El campo FileSystemName debe contener el nombre del sistema de archivos en el volumen.

El valor válido para este campo es, en caracteres ASCII, "EX EX" , que incluye tres espacios en blanco finales.

#### <a name="313-mustbezero-field"></a>3.1.3 Campo MustBeZero

El campo MustBeZero debe corresponderse directamente con el intervalo de bytes que el bloque de parámetros BIOS empaquetado consume en volúmenes FAT12/16/32.

El valor válido para este campo es 0, lo que ayuda a evitar que las implementaciones FAT12/16/32 monten erróneamente un volumen ex RAID.

#### <a name="314-partitionoffset-field"></a>3.1.4 Campo PartitionOffset

El campo PartitionOffset debe describir el desplazamiento del sector relativo a los medios de la partición que hospeda el volumen ex RAID especificado. Este campo ayuda a arrancar el arranque desde el volumen mediante la extensión INT 13h en equipos personales.

Todos los valores posibles para este campo son válidos; sin embargo, el valor 0 indica que las implementaciones omitirán este campo.

#### <a name="315-volumelength-field"></a>3.1.5 Campo VolumeLength

El campo VolumeLength debe describir el tamaño del volumen ex EX EXL dado en los sectores.

El intervalo válido de valores para este campo debe ser:

- Al menos<sup>2 20/2</sup><sup>bytesPerSectorShift,</sup>lo que garantiza que el volumen más pequeño no sea inferior a 1 MB.

- Como máximo 2<sup>64</sup>- 1, el valor más grande que este campo puede describir

Sin embargo, si el tamaño de la subruta Espacio excesivo es 0, el valor de este campo es ClusterHeapOffset + (2<sup>32</sup>- 11) \* 2<sup>SectorPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 Campo FatOffset

El campo FatOffset debe describir el desplazamiento del sector relativo al volumen de first FAT. Este campo permite a las implementaciones alinear first FAT con las características de los medios de almacenamiento subyacentes.

El intervalo válido de valores para este campo debe ser:

- Al menos 24, que tienen en cuenta los sectores que consumen las regiones arranque principal y arranque de copia de seguridad.

- A lo sumo ClusterHeapOffset - (FatLength NumberOfAturas), que tiene en cuenta los sectores que consume el \* montón de clústeres

#### <a name="317-fatlength-field"></a>3.1.7 FatLength Field

El campo FatLength debe describir la longitud, en sectores, de cada tabla FAT (el volumen puede contener hasta dos FAT).

El intervalo válido de valores para este campo debe ser:

- Al menos (ClusterCount + 2) \* 2<sup>2/2</sup><sup>BytesPerSectorShift</sup>redondeado al entero más cercano, lo que garantiza que cada FAT tenga espacio suficiente para describir todos los clústeres del montón de clústeres.

- Como máximo (ClusterHeapOffset - FatOffset) / NumberOfPlants redondeado al entero más cercano, lo que garantiza que las FAT existen antes que el montón de clústeres

Este campo puede contener un valor que supere su límite inferior (como se describió anteriormente) para permitir que la segunda FAT, si está presente, también se alinee con las características del medio de almacenamiento subyacente. El contenido del espacio que supera lo que el propio FAT requiere, si lo hay, no están definidos.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 Campo ClusterHeapOffset

El campo ClusterHeapOffset debe describir el desplazamiento del sector relativo al volumen del montón de clúster. Este campo permite a las implementaciones alinear el montón de clúster con las características de los medios de almacenamiento subyacentes.

El intervalo válido de valores para este campo debe ser:

- Al menos FatOffset + FatLength NumberOfPlants, para tener en cuenta los sectores que consumen \* todas las regiones anteriores.

- Como máximo 2<sup>32</sup>- 1 o VolumeLength - (ClusterCount \* 2<sup>SectorsPerClusterShift),</sup>el cálculo que sea menor

#### <a name="319-clustercount-field"></a>3.1.9 Campo ClusterCount

El campo ClusterCount debe describir el número de clústeres que contiene el montón de clústeres.

El valor válido para este campo debe ser el menor de los siguientes:

- (VolumeLength - ClusterHeapOffset) / 2<sup>SectorPerClusterShift</sup>redondeado al entero más cercano, que es exactamente el número de clústeres que pueden caber entre el principio del montón de clústeres y el final del volumen.

- 2<sup>32</sup>- 11, que es el número máximo de clústeres que un FAT puede describir

El valor del campo ClusterCount determina el tamaño mínimo de fat. Para evitar las FAT extremadamente grandes, las implementaciones pueden controlar el número de clústeres en el montón de clústeres aumentando el tamaño del clúster (a través del campo SectorsPerClusterShift). Esta especificación no recomienda más de<sup>2 24</sup>- 2 clústeres en el montón de clústeres. Sin embargo, las implementaciones podrán controlar volúmenes con hasta<sup>2 32</sup>-11 clústeres en el montón de clústeres.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 Campo FirstClusterOfRootDirectory

El campo FirstClusterOfRootDirectory debe contener el índice del clúster del primer clúster del directorio raíz. Las implementaciones deben hacer todo lo posible para colocar el primer clúster del directorio raíz en el primer clúster no malo después de los clústeres que consumen el mapa de bits de asignación y la tabla de mayúsculas y minúsculas.

El intervalo válido de valores para este campo debe ser:

- Al menos 2, el índice del primer clúster del montón de clústeres

- Como máximo ClusterCount + 1, el índice del último clúster del montón de clústeres

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 Campo VolumeSerialNumber

El campo VolumeSerialNumber debe contener un número de serie único. Esto ayuda a las implementaciones a distinguir entre diferentes volúmenes ex EX EX EX.
Las implementaciones deben generar el número de serie mediante la combinación de la fecha y hora de formato del volumen ex SERIAL. El mecanismo para combinar la fecha y hora para formar un número de serie es específico de la implementación.

Todos los valores posibles para este campo son válidos.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 FileSystemRevision Field

El campo FileSystemRevision debe describir los números de revisión principales y menores de las estructuras ex RAID en el volumen dado.

El byte de orden superior es el número de revisión principal y el byte de orden bajo es el número de revisión secundaria. Por ejemplo, si el byte de orden superior contiene el valor 01h y el byte de orden bajo contiene el valor 05h, el campo FileSystemRevision describe el número de revisión 1.05.
Del mismo modo, si el byte de orden superior contiene el valor 0Ah y el byte de orden bajo contiene el valor 0Fh, el campo FileSystemRevision describe el número de revisión 10.15.

El intervalo válido de valores para este campo debe ser:

- Al menos 0 para el byte de orden bajo y 1 para el byte de orden superior

- Como máximo 99 para el byte de orden bajo y 99 para el byte de orden superior

El número de revisión de ex EX EX QUE describe esta especificación es 1.00.
Las implementaciones de esta especificación deben montar cualquier volumen ex EX CON el número de revisión principal 1 y no montar ningún volumen ex RAID con ningún otro número de revisión principal. Las implementaciones respetarán el número de revisión menor y no realizarán operaciones ni crearán estructuras del sistema de archivos no descritas en la especificación correspondiente del número de revisión menor especificado.

#### <a name="3113-volumeflags-field"></a>3.1.13 Campo VolumeFlags

El campo VolumeFlags debe contener marcas que indiquen el estado de varias estructuras del sistema de archivos en el volumen ex RAID (consulte [la tabla 5).](#table-5-volumeflags-field-structure)

Las implementaciones no deben incluir este campo al calcular su suma de comprobación correspondiente de la región de arranque principal o de arranque de copia de seguridad. Al hacer referencia al sector de arranque de copia de seguridad, las implementaciones deben tratar este campo como obsoleto.

<div id="table-5-volumeflags-field-structure" />

**Estructura del campo VolumeFlags de la tabla 5**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveGraba</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#31131-activefat-field">la sección 3.1.13.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#31132-volumedirty-field">la sección 3.1.13.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#31133-mediafailure-field">la sección 3.1.13.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#31134-cleartozero-field">la sección 3.1.13.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>4</td>
<td>12</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 Campo Active Ya

El campo ActiveAtura debe describir qué FAT y Mapa de bits de asignación están activos (y las implementaciones deben usar), como se muestra a continuación:

- 0, lo que significa que los mapas de bits First FAT y First Allocation Bitmap están activos

- 1, lo que significa que el segundo mapa de bits de asignación FAT y segundo están activos y solo es posible cuando el campo NumberOfAturas contiene el valor 2.

Las implementaciones deben considerar el fat inactivo y el mapa de bits de asignación como obsoletos. Solo las implementaciones que tienen en cuenta La Forma de trabajo de Texas deben cambiar los mapas de bits activos de asignación y FAT (consulte [la sección 7.1).](#71-allocation-bitmap-directory-entry)

##### <a name="31132-volumedirty-field"></a>3.1.13.2 Campo VolumeDirty

El campo VolumeDirty debe describir si el volumen está sucio o no, como se indica a continuación:

- 0, lo que significa que el volumen probablemente esté en un estado coherente

- 1, lo que significa que el volumen probablemente esté en un estado incoherente

Las implementaciones deben establecer el valor de este campo en 1 al encontrar incoherencias de metadatos del sistema de archivos que no resuelven. Si, al montar un volumen, el valor de este campo es 1, solo las implementaciones que resuelven incoherencias de metadatos del sistema de archivos pueden borrar el valor de este campo en 0. Estas implementaciones solo borrarán el valor de este campo en 0 después de asegurarse de que el sistema de archivos está en un estado coherente.

Si, al montar un volumen, el valor de este campo es 0, las implementaciones deben establecer este campo en 1 antes de actualizar los metadatos del sistema de archivos y borrar este campo en 0 posteriormente, de forma similar a la ordenación de escritura recomendada descrita en la [sección 8.1](#81-recommended-write-ordering).

##### <a name="31133-mediafailure-field"></a>3.1.13.3 Campo MediaFailure

El campo MediaFailure debe describir si una implementación ha detectado errores multimedia o no, como se indica a continuación:

- 0, lo que significa que el medio de hospedaje no ha notificado errores o que los errores conocidos ya están registrados en el FAT como clústeres "malo".

- 1, lo que significa que el medio de hospedaje ha notificado errores (es decir, se han registrado errores en las operaciones de lectura o escritura).

Una implementación debe establecer este campo en 1 cuando:

1. El medio de hospedaje produce un error en los intentos de acceso a cualquier región del volumen.

2. La implementación ha agotado los algoritmos de reintento de acceso, si los hay.

Si, al montar un volumen, el valor de este campo es 1, las implementaciones que analizan todo el volumen en busca de errores multimedia y registran todos los errores como clústeres "no válidos" en FAT (o resuelven errores de medios) pueden borrar el valor de este campo en 0.

##### <a name="31134-cleartozero-field"></a>3.1.13.4 Campo ClearToZero

El campo ClearToZero no tiene un significado significativo en esta especificación.

Los valores válidos para este campo son:

- 0, que no tiene ningún significado concreto

- 1, lo que significa que las implementaciones deben borrar este campo a 0 antes de modificar las estructuras, directorios o archivos del sistema de archivos.

#### <a name="3114-bytespersectorshift-field"></a>Campo 3.1.14 BytesPerSectorShift

El campo BytesPerSectorShift debe describir los bytes por sector expresados como registro<sub>2</sub>(N), donde N es el número de bytes por sector. Por ejemplo, para 512 bytes por sector, el valor de este campo es 9.

El intervalo válido de valores para este campo debe ser:

- Al menos 9 (tamaño de sector de 512 bytes), que es el sector más pequeño posible para un volumen ex BYTE

- Como máximo 12 (tamaño de sector de 4096 bytes), que es el tamaño de página de memoria de las CPU comunes en equipos personales

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 SectoresPerClusterShift Field

El campo SectorsPerClusterShift debe describir los sectores por clúster expresados como registro<sub>2</sub>(N), donde N es el número de sectores por clúster. Por ejemplo, para 8 sectores por clúster, el valor de este campo es 3.

El intervalo válido de valores para este campo debe ser:

- Al menos 0 (1 sector por clúster), que es el clúster más pequeño posible

- Como máximo 25 - BytesPerSectorShift, que se evalúa como un tamaño de clúster de 32 MB

#### <a name="3116-numberoffats-field"></a>3.1.16 Campo NumberOf Yas

El campo NumberOfPlants debe describir el número de mapas de bits de asignación y las FAT que contiene el volumen.

El intervalo válido de valores para este campo debe ser:

- 1, que indica que el volumen solo contiene los mapas de bits First FAT y First Allocation

- 2, que indica que el volumen contiene los mapas de bits First FAT, Second FAT, First Allocation Bitmap y Second Allocation Bitmap; este valor solo es válido para los volúmenes de Texas RAID.

#### <a name="3117-driveselect-field"></a>3.1.17 UnidadSeleccionar campo

El campo DriveSelect debe contener el número de unidad INT 13h extendido, lo que ayuda a arrancar desde este volumen mediante int extendido de 13 h en equipos personales.

Todos los valores posibles para este campo son válidos. Los campos similares de los sistemas de archivos basados en FAT anteriores contenían con frecuencia el valor 80h.

#### <a name="3118-percentinuse-field"></a>Campo PercentInUse de 3.1.18

El campo PercentInUse debe describir el porcentaje de clústeres del montón de clústeres que se asignan.

El intervalo válido de valores para este campo debe ser:

- Entre 0 y 100 inclusive, que es el porcentaje de clústeres asignados en el montón de clústeres, redondeados hacia abajo al entero más cercano

- Exactamente FFh, que indica que el porcentaje de clústeres asignados en el montón de clústeres no está disponible

Las implementaciones deben cambiar el valor de este campo para reflejar los cambios en la asignación de clústeres en el montón de clústeres o lo cambiarán a FFh.

Las implementaciones no deben incluir este campo al calcular su suma de comprobación correspondiente de la región de arranque principal o de arranque de copia de seguridad. Al hacer referencia al sector de arranque de copia de seguridad, las implementaciones deben tratar este campo como obsoleto.

#### <a name="3119-bootcode-field"></a>3.1.19 Campo BootCode

El campo BootCode debe contener instrucciones de arranque.
Las implementaciones pueden rellenar este campo con las instrucciones de CPU necesarias para arrancar un sistema informático. Las implementaciones que no proporcionan instrucciones de arranque de arranque inicializarán cada byte de este campo en F4h (la instrucción de detención de CPU comunes en equipos personales) como parte de su operación de formato.

#### <a name="3120-bootsignature-field"></a>3.1.20 BootSignature Field

El campo BootSignature debe describir si la intención de un sector determinado es que sea un sector de arranque o no.

El valor válido para este campo es AA55h. Cualquier otro valor de este campo invalida su respectivo sector de arranque. Las implementaciones deben comprobar el contenido de este campo antes de que dependa de cualquier otro campo de su respectivo sector de arranque.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3.2 Subrecciones de sectores de arranque extendidos principales y de copia de seguridad

Cada sector de los principales sectores de arranque extendido tiene la misma estructura; sin embargo, cada sector puede contener instrucciones de arranque distintas (consulte la tabla 6). Los agentes de arranque, como las instrucciones de arranque del sector de arranque principal, las implementaciones de BIOS alternativas o el firmware de un sistema insertado, pueden cargar estos sectores y ejecutar las instrucciones que contienen.

Los sectores de arranque extendido de copia de seguridad son una copia de seguridad de los principales sectores de arranque extendido y tienen la misma estructura (consulte [la tabla 6).](#table-6-extended-boot-sector-structure)

Antes de ejecutar las instrucciones de los sectores de arranque principal o de copia de seguridad extendida, las implementaciones deben comprobar su contenido asegurándose de que el campo ExtendedBootSignature de cada sector contiene su valor prescrito.

Aunque la operación de formato inicial inicializará el contenido de los sectores de arranque extendido principal y de copia de seguridad, las implementaciones pueden actualizar estos sectores (y también actualizar sus respectivas sumas de comprobación de arranque) según sea necesario.

<div id="table-6-extended-boot-sector-structure" />

**Tabla 6 Estructura del sector de arranque extendido**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>bytesPerSectorShift</sup> – 4</td>
<td><p>Este campo es obligatorio y <a href="#321-extendedbootcode-field">la sección 3.2.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>bytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Este campo es obligatorio y <a href="#322-extendedbootsignature-field">la sección 3.2.2</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 Campo ExtendedBootCode

El campo ExtendedBootCode debe contener instrucciones de arranque.
Las implementaciones pueden rellenar este campo con las instrucciones de CPU necesarias para arrancar un sistema informático. Las implementaciones que no proporcionan instrucciones de arranque de arranque inicializarán cada byte de este campo en 00h como parte de su operación de formato.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 Campo ExtendedBootSignature

El campo ExtendedBootSignature debe describir si la intención de un sector determinado es que sea un sector de arranque extendido o no.

El valor válido para este campo es AA550000h. Cualquier otro valor de este campo invalida su respectivo sector de arranque extendido principal o de copia de seguridad.
Las implementaciones deben comprobar el contenido de este campo antes de, en función de cualquier otro campo de su respectivo sector de arranque extendido.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3.3 Subrecciones de parámetros de OEM principales y de copia de seguridad

La subr regiones Parámetros principales de OEM contiene diez estructuras de parámetros que pueden contener información específica del fabricante (consulte [la tabla 7).](#table-7-oem-parameters-structure) Cada una de las diez estructuras de parámetros se deriva de la plantilla Parámetros genéricos (consulte [la sección 3.3.2).](#332-generic-parameters-template) Los fabricantes pueden derivar sus propias estructuras de parámetros personalizados de la plantilla Parámetros genéricos. Esta especificación define dos estructuras de parámetros: parámetros NULL (consulte la sección [3.3.3)](#333-null-parameters)y parámetros flash (consulte la sección [3.3.4).](#334-flash-parameters)

Los parámetros de OEM de copia de seguridad son una copia de seguridad de los parámetros principales de OEM y tienen la misma estructura (consulte [la tabla 7).](#table-7-oem-parameters-structure)

Antes de usar el contenido de los parámetros MAIN o Backup OEM, las implementaciones deben comprobar su contenido validando su respectiva suma de comprobación de arranque.

Los fabricantes deben rellenar los parámetros de OEM Main y Backup con sus propias estructuras de parámetros personalizados, si las hubiera, y cualquier otra estructura de parámetros. Las operaciones de formato posteriores conservarán el contenido de los parámetros de OEM Main y Backup.

Las implementaciones pueden actualizar los parámetros principal y de oem de copia de seguridad según sea necesario (y también actualizar sus respectivas sumas de comprobación de arranque).

<div id="table-7-oem-parameters-structure" />

**Tabla 7 Estructura de parámetros de OEM**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parámetros[0]</td>
<td>0</td>
<td>48</td>
<td>Este campo es obligatorio y <a href="#331-parameters0--parameters9">la sección 3.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Parámetros[9]</td>
<td>432</td>
<td>48</td>
<td>Este campo es obligatorio y <a href="#331-parameters0--parameters9">la sección 3.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>480</td>
<td>2<sup>bytesPerSectorShift</sup> – 480</td>
<td><p>Este campo es obligatorio y su contenido está reservado.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 Parámetros \[ 0 \] ... Parámetros \[ 9\]

Cada campo Parameters de esta matriz contiene una estructura de parámetros, que deriva de la plantilla Parámetros genéricos (consulte [la sección 3.3.2).](#332-generic-parameters-template)
Cualquier campo Parámetros no usado debe describirse como que contiene una estructura Parámetros NULL (consulte [la sección 3.3.3).](#333-null-parameters)

#### <a name="332-generic-parameters-template"></a>3.3.2 Plantilla de parámetros genéricos

La plantilla Parámetros genéricos proporciona la definición base de una estructura de parámetros (vea [la tabla 8).](#table-8-generic-parameters-template) Todas las estructuras de parámetros derivan de esta plantilla. La compatibilidad con esta plantilla de parámetros genéricos es obligatoria.

<div id="table-8-generic-parameters-template" />

**Plantilla de parámetros genéricos de la tabla 8**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#3321-parametersguid-field">la sección 3.3.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla definen su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 ParametersGuid Field

El campo ParametersGuid debe describir un GUID, que determina el diseño del resto de la estructura de parámetros especificada.

Todos los valores posibles para este campo son válidos; Sin embargo, los fabricantes deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al derivar estructuras de parámetros personalizados de esta plantilla.

#### <a name="333-null-parameters"></a>3.3.3 Parámetros null

La estructura Parámetros null se deriva de la plantilla Parámetros genéricos (consulte la sección [3.3.2)](#332-generic-parameters-template)y describirá un campo Parámetros sin usar (vea [la tabla 9).](#table-9-null-parameters-structure) Al crear o actualizar la estructura Parámetros de OEM, las implementaciones rellenarán los campos parámetros no usados con la estructura Parámetros null. Además, al crear o actualizar la estructura Parámetros de OEM, las implementaciones deben consolidar las estructuras de parámetros NULL al final de la matriz, lo que deja todas las demás estructuras parameters al principio de la estructura Parámetros de OEM.

La compatibilidad con la estructura Parámetros NULL es obligatoria.

<div id="table-9-null-parameters-structure" />

**Estructura de parámetros NULL de la tabla 9**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#3331-parametersguid-field">la sección 3.3.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>16</td>
<td>32</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 ParametersGuid Field

El campo ParametersGuid se ajustará a la definición proporcionada por la plantilla Parámetros genéricos (consulte la [sección 3.3.2.1).](#3321-parametersguid-field)

El valor válido para este campo, en la notación GUID, es {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>3.3.4 Parámetros flash

La estructura de parámetros flash se deriva de la plantilla Parámetros genéricos (consulte la sección [3.3.2)](#332-generic-parameters-template)y contiene parámetros para medios flash (consulte la [tabla 10).](#table-10-flash-parameters-structure) Los fabricantes de dispositivos de almacenamiento basados en flash pueden rellenar un campo Parámetros (preferiblemente el campo Parámetros \[ \] 0) con esta estructura de parámetros. Las implementaciones pueden usar la información de la estructura Parámetros flash para optimizar las operaciones de acceso durante las lecturas y escrituras y para la alineación de las estructuras del sistema de archivos que dura el formato de los medios.

La compatibilidad con la estructura Parámetros flash es opcional.

<div id="table-10-flash-parameters-structure" />

**Tabla 10 Estructura de parámetros flash**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#3341-parametersguid-field">la sección 3.3.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3342-eraseblocksize-field">la sección 3.3.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3343-pagesize-field">la sección 3.3.4.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3344-sparesectors-field">la sección 3.3.4.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3345-randomaccesstime-field">la sección 3.3.4.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3346-programmingtime-field">la sección 3.3.4.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3347-readcycle-field">la sección 3.3.4.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#3348-writecycle-field">la sección 3.3.4.8</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>44</td>
<td>4</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

Todos los valores posibles de todos los campos de parámetros flash, excepto el campo ParametersGuid, son válidos. Sin embargo, el valor 0 indica que el campo realmente no tiene sentido (las implementaciones omitirán el campo especificado).

##### <a name="3341-parametersguid-field"></a>3.3.4.1 ParametersGuid Field

El campo ParametersGuid se ajustará a la definición proporcionada en la plantilla Parámetros genéricos (consulte [la sección 3.3.2.1).](#3321-parametersguid-field)

El valor válido para este campo, en la notación GUID, es {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 Campo EraseBlockSize

El campo EraseBlockSize describirá el tamaño, en bytes, del bloque de borrado del medio flash.

##### <a name="3343-pagesize-field"></a>3.3.4.3 Campo PageSize

El campo PageSize debe describir el tamaño, en bytes de la página del medio flash.

##### <a name="3344-sparesectors-field"></a>3.3.4.4 Campo SpareSectors

El campo SpareSectors describirá el número de sectores que el medio flash tiene disponible para sus operaciones internas de moderación.

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 Campo RandomAccessTime

El campo RandomAccessTime describirá el tiempo medio de acceso aleatorio de los medios flash, en nanosegundos.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 Campo ProgrammingTime

El campo ProgrammingTime describirá el tiempo medio de programación de los medios flash, en nanosegundos.

##### <a name="3347-readcycle-field"></a>3.3.4.7 Campo ReadCycle

El campo ReadCycle describirá el tiempo medio de ciclo de lectura de los medios flash, en nanosegundos.

##### <a name="3348-writecycle-field"></a>3.3.4.8 Campo WriteCycle

El campo WriteCycle describirá el tiempo medio del ciclo de escritura, en nanosegundos.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3.4 Subrecciones de suma de comprobación principal y de arranque de copia de seguridad

Las sumas de comprobación principal y de arranque de copia de seguridad contienen cada una un patrón de repetición de la suma de comprobación de cuatro bytes del contenido de todas las demás subrecciones en sus respectivas regiones de arranque. El cálculo de suma de comprobación no debe incluir los campos VolumeFlags y PercentInUse en sus respectivos sectores de arranque (consulte [la figura 1).](#figure-1-boot-checksum-computation) El patrón de repetición de la suma de comprobación de cuatro bytes rellena su subrecciones de suma de comprobación de arranque correspondientes desde el principio hasta el final de la subrecciones.

Antes de usar el contenido de cualquiera de las otras regiones en las regiones Main o Backup Boot, las implementaciones deben comprobar su contenido validando su respectiva suma de comprobación de arranque.

Aunque la operación de formato inicial rellenará las sumas de comprobación principal y de arranque de copia de seguridad con el patrón de suma de comprobación que se repite, las implementaciones actualizarán estos sectores a medida que cambie el contenido de los otros sectores de sus respectivas regiones de arranque.

<div id="figure-1-boot-checksum-computation" />

**Figura 1 Cálculo de suma de comprobación de arranque**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4 Región de tabla de asignación de archivos

La región De tabla de asignación de archivos (FAT) puede contener hasta dos FAT, una en la subr regiones First FAT y otra en la segunda subr region fat.
El campo NumberOfLats describe el número de FAT que contiene esta región. Los valores válidos para el campo NumberOfPlants son 1 y 2. Por lo tanto, la primera sub-región FAT siempre contiene un FAT. Si el campo NumberOfAturas es dos, la segunda subrecciones FAT también contiene una fat.

El campo ActiveAtura del campo VolumeFlags describe qué FAT está activo. Solo el campo VolumeFlags del sector de arranque principal está actual.
Las implementaciones deben tratar el FAT que no está activo como obsoleto. El uso de FAT inactivo y el cambio entre las FAT son específicos de la implementación.

### <a name="41-first-and-second-fat-sub-regions"></a>4.1 Subrecciones FAT de primera y segunda

Una FAT describirá las cadenas de clúster en el montón de clúster (consulte [la tabla 11).](#table-11-file-allocation-table-structure)
Una cadena de clústeres es una serie de clústeres que proporciona espacio para registrar el contenido de archivos, directorios y otras estructuras del sistema de archivos. FAT representa una cadena de clúster como una lista de índices de clúster vinculadas de forma singly. A excepción de las dos primeras entradas, cada entrada de fat representa exactamente un clúster.

<div id="table-11-file-allocation-table-structure" />

**Tabla 11 Estructura de tabla de asignación de archivos**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry[0]</td>
<td>0</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#412-fatentry1-field">la sección 4.1.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FatEntry[1]</td>
<td>4</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#412-fatentry1-field">la sección 4.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FatEntry[2]</td>
<td>8</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#413-fatentry2--fatentryclustercount1-fields">la sección 4.1.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry[ClusterCount+1]</td>
<td>(ClusterCount + 1) * 4</td>
<td>4</td>
<td><p>Este campo es obligatorio y <a href="#413-fatentry2--fatentryclustercount1-fields">la sección 4.1.3</a> define su contenido.</p>
<p>ClusterCount + 1 nunca puede superar FFFFFFF6h.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(ClusterCount + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((ClusterCount + 2) * 4)</td>
<td><p>Este campo es obligatorio y su contenido, si existe, no está definido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos ClusterCount, FatLength y BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 Campo FatEntry \[ 0 \]

El campo FatEntry 0 describirá el tipo de medio en el primer byte (el byte de orden más bajo) y contendrá FFh en los \[ \] tres bytes restantes.

El tipo de medio (el primer byte) debe ser F8h.

#### <a name="412-fatentry1-field"></a>4.1.2 Campo FatEntry \[ 1 \]

El campo FatEntry \[ 1 \] solo existe debido a la precedencia histórica y no describe nada de interés.

El valor válido para este campo es FFFFFFFFh. Las implementaciones inicializarán este campo en su valor prescrito y no deben usar este campo para ningún propósito. Las implementaciones no deben interpretar este campo y deben conservar su contenido en todas las operaciones que modifican los campos circundantes.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... Campos FatEntry \[ ClusterCount+1 \]

Cada campo FatEntry de esta matriz debe representar un clúster en el montón de clúster. FatEntry 2 representa el primer clúster del montón de clúster y \[ \] FatEntry \[ ClusterCount+1 representa el último \] clúster del montón de clúster.

El intervalo válido de valores para estos campos debe ser:

- Entre 2 y ClusterCount + 1, ambos incluidos, que apuntan al siguiente FatEntry en la cadena de clúster dada; el fatEntry dado no debe apuntar a ninguna FatEntry que le preceda en la cadena de clúster determinada

- Exactamente FFFFFFF7h, que marca el clúster correspondiente de FatEntry dado como "malo"

- Exactamente FFFFFFFFh, que marca el clúster correspondiente de FatEntry dado como el último clúster de una cadena de clúster; este es el único valor válido para el último FatEntry de cualquier cadena de clúster determinada

## <a name="5-data-region"></a>5 Región de datos

La región Datos contiene el montón de clúster, que proporciona espacio administrado para estructuras, directorios y archivos del sistema de archivos.

### <a name="51-cluster-heap-sub-region"></a>5.1 Subr regiones del montón de clúster

La estructura del montón de clúster es muy sencilla (vea [la tabla 12](#table-12-cluster-heap-structure)); cada serie consecutiva de sectores describe un clúster, como define el campo SectorsPerClusterShift. Lo importante es que el primer clúster del montón de clústeres tiene el índice dos, que corresponde directamente al índice de FatEntry \[ \] 2.

En un volumen ex RAID, un mapa de bits de asignación (consulte la sección [7.1.5)](#715-allocation-bitmap)mantiene el registro del estado de asignación de todos los clústeres. Se trata de una diferencia significativa con respecto a los predecesores de exAPI (FAT12, FAT16 y FAT32), en los que fat mantiene un registro del estado de asignación de todos los clústeres del montón de clústeres.

<div id="table-12-cluster-heap-structure" />

**Tabla 12 Estructura del montón de clúster**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(sector)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(sectores)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Clúster[2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectoresPerClusterShift</sup></td>
<td><p>Este campo es obligatorio y <a href="#511-cluster2--clusterclustercount1-fields">la sección 5.1.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset y SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster[ClusterCount+1]</td>
<td>ClusterHeapOffset + (ClusterCount – 1) * 2<sup>SectoresPerClusterShift</sup></td>
<td>2<sup>SectoresPerClusterShift</sup></td>
<td><p>Este campo es obligatorio y <a href="#511-cluster2--clusterclustercount1-fields">la sección 5.1.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen los campos ClusterCount, ClusterHeapOffset y SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Clúster \[ 2 \] ... Cluster \[ ClusterCount+1 \] Campos

Cada campo Cluster de esta matriz es una serie de sectores contiguos, cuyo tamaño se define mediante el campo SectorsPerClusterShift.

## <a name="6-directory-structure"></a>6 Estructura de directorios

El sistema de archivos exSTRUCCIONES usa un enfoque de árbol de directorios para administrar las estructuras del sistema de archivos y los archivos que existen en el montón de clúster. Los directorios tienen una relación uno a varios entre el elemento primario y el secundario en el árbol de directorios.

El directorio al que hace referencia el campo FirstClusterOfRootDirectory es la raíz del árbol de directorios. Todos los demás directorios descienden del directorio raíz de forma vinculada de forma singly.

Cada directorio consta de una serie de entradas de directorio (vea [la tabla 13).](#table-13-directory-structure)

Una o varias entradas de directorio se combinan en un conjunto de entradas de directorio que describe algo de interés, como una estructura del sistema de archivos, un directorio o un archivo.

<div id="table-13-directory-structure" />

**Tabla 13 Estructura de directorios**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry[0]</td>
<td>0</td>
<td>32</td>
<td>Este campo es obligatorio y <a href="#61-directoryentry0--directoryentryn--1">la sección 6.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry[N–1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Este campo es obligatorio y <a href="#61-directoryentry0--directoryentryn--1">la sección 6.1</a> define su contenido.</p>
<p>N, el número de campos DirectoryEntry, es el tamaño, en bytes, de la cadena de clúster que contiene el directorio especificado, dividido por el tamaño de un campo DirectoryEntry, 32 bytes.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6.1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Cada campo DirectoryEntry de esta matriz se deriva de la plantilla Generic DirectoryEntry (consulte [la sección 6.2).](#62-generic-directoryentry-template)

### <a name="62-generic-directoryentry-template"></a>6.2 Plantilla Generic DirectoryEntry

La plantilla Generic DirectoryEntry proporciona la definición base para las entradas de directorio (vea [la tabla 14).](#table-14-generic-directoryentry-template) Todas las estructuras de entrada de directorio derivan de esta plantilla y solo las estructuras de entrada de directorio definidas por Microsoft son válidas (ex LDAP no tiene aprovisionamientos para las estructuras de entrada de directorio definidas por el fabricante, excepto como se define en la sección [7.8](#78-vendor-extension-directory-entry) y [la sección 7.9).](#79-vendor-allocation-directory-entry) La capacidad de interpretar la plantilla Generic DirectoryEntry es obligatoria.

<div id="table-14-generic-directoryentry-template" />

**Tabla 14 Generic DirectoryEntry Template**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#621-entrytype-field">la sección 6.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla pueden definir su contenido.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#622-firstcluster-field">la sección 6.2.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#623-datalength-field">la sección 6.2.3</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 Campo EntryType

El campo EntryType tiene tres modos de uso que define el valor del campo (vea la lista siguiente).

- 00h, que es un marcador de fin de directorio y se aplican las condiciones siguientes:

  - Todos los demás campos del DirectoryEntry especificado están reservados realmente

  - Todas las entradas de directorio subsiguientes del directorio especificado también son marcadores de fin de directorio

  - Los marcadores de fin de directorio solo son válidos fuera de los conjuntos de entrada de directorio

  - Las implementaciones pueden sobrescribir los marcadores de fin de directorio según sea necesario.

- Entre 01h y 7Fh inclusive, que es un marcador de entrada de directorio sin usar y se aplican las condiciones siguientes:

  - Todos los demás campos del DirectoryEntry especificado no están definidos realmente

  - Las entradas de directorio no utilizadas solo son válidas fuera de los conjuntos de entrada de directorio

  - Las implementaciones pueden sobrescribir las entradas de directorio no utilizadas según sea necesario.

  - Este intervalo de valores corresponde al campo InUse (consulte la sección [6.2.1.4)](#6214-inuse-field)que contiene el valor 0.

- Entre 81 h y FFh inclusive, que es una entrada de directorio normal y se aplican las condiciones siguientes:

  - El contenido del campo EntryType (consulte [la tabla 15)](#table-15-generic-entrytype-field-structure)determina el diseño del resto de la estructura DirectoryEntry.

  - Este intervalo de valores, y solo este intervalo de valores, son válidos dentro de un conjunto de entradas de directorio

  - Este intervalo de valores corresponde directamente al campo InUse (consulte la sección [6.2.1.4)](#6214-inuse-field)que contiene el valor 1.

Para evitar modificaciones en el campo InUse (consulte la sección [6.2.1.4)](#6214-inuse-field)que da lugar erróneamente a un marcador de fin de directorio, el valor 80h no es válido.

<div id="table-15-generic-entrytype-field-structure" />

**Tabla 15 Estructura de campo EntryType genérica**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Este campo es obligatorio y <a href="#6211-typecode-field">la sección 6.2.1.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>Este campo es obligatorio y la sección <a href="#6212-typeimportance-field">6.2.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6213-typecategory-field">la sección 6.2.1.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6214-inuse-field">la sección 6.2.1.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 Campo TypeCode

El campo TypeCode describe parcialmente el tipo específico de la entrada de directorio determinada. Este campo, además de los campos TypeImportance y TypeCategory (vea sección [6.2.1.2](#6212-typeimportance-field) y sección [6.2.1.3,](#6213-typecategory-field)respectivamente), identifica de forma única el tipo de la entrada de directorio determinada.

Todos los valores posibles de este campo son válidos, a menos que los campos TypeImportance y TypeCategory contengan el valor 0; En ese caso, el valor 0 no es válido para este campo.

##### <a name="6212-typeimportance-field"></a>6.2.1.2 Campo TypeImportance

El campo TypeImportance describirá la importancia de la entrada de directorio determinada.

Los valores válidos para este campo deben ser:

- 0, lo que significa que la entrada de directorio dada es crítica (consulte la [sección 6.3.1.2.1](#63121-critical-primary-directory-entries) y la sección [6.4.1.2.1](#64121-critical-secondary-directory-entries) para las entradas de directorio principal y secundaria críticas, respectivamente).

- 1, lo que significa que la entrada de directorio dada es benigna (consulte la sección [6.3.1.2.2](#63122-benign-primary-directory-entries) y la [sección 6.4.1.2.2 para](#64122-benign-secondary-directory-entries) las entradas benignas de directorio principal e secundario benigno, respectivamente).

##### <a name="6213-typecategory-field"></a>6.2.1.3 Campo TypeCategory

El campo TypeCategory describirá la categoría de la entrada de directorio determinada.

Los valores válidos para este campo deben ser:

- 0, lo que significa que la entrada de directorio determinada es principal (consulte [la sección 6.3)](#63-generic-primary-directoryentry-template)

- 1, lo que significa que la entrada de directorio dada es secundaria (consulte [la sección 6.4)](#64-generic-secondary-directoryentry-template)

##### <a name="6214-inuse-field"></a>6.2.1.4 Campo InUse

El campo InUse debe describir si la entrada de directorio determinada está en uso o no.

Los valores válidos para este campo deben ser:

- 0, lo que significa que la entrada de directorio determinada no está en uso; esto significa que la estructura dada es realmente una entrada de directorio sin usar

- 1, lo que significa que la entrada de directorio determinada está en uso; esto significa que la estructura dada es una entrada de directorio normal.

#### <a name="622-firstcluster-field"></a>6.2.2 Campo FirstCluster

El campo FirstCluster debe contener el índice del primer clúster de una asignación en el montón de clúster asociado a la entrada de directorio determinada.

El intervalo válido de valores para este campo debe ser:

- Exactamente 0, lo que significa que no existe ninguna asignación de clúster

- Entre 2 y ClusterCount + 1, que es el intervalo de índices de clúster válidos

Las estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DataLength, si una asignación de clúster no es compatible con la estructura derivada.

#### <a name="623-datalength-field"></a>6.2.3 Campo DataLength

El campo DataLength describe el tamaño, en bytes, de los datos que contiene la asignación de clúster asociada.

El intervalo de valor válido para este campo es:

- Al menos 0; si el campo FirstCluster contiene el valor 0, el único valor válido de este campo es 0.

- Como máximo ClusterCount \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Las estructuras que derivan de esta plantilla pueden redefinir los campos FirstCluster y DataLength, si no es posible una asignación de clúster para la estructura derivada.

### <a name="63-generic-primary-directoryentry-template"></a>6.3 Directorio principal genérico TemplateEntry

La primera entrada de directorio de un conjunto de entradas de directorio debe ser una entrada de directorio principal. Todas las entradas de directorio subsiguientes, si las hay, en el conjunto de entradas de directorio deben ser entradas de directorio secundario (consulte [la sección 6.4).](#64-generic-secondary-directoryentry-template)

La capacidad de interpretar la plantilla Generic Primary DirectoryEntry es obligatoria.

Todas las estructuras de entrada del directorio principal derivan de la plantilla Generic Primary DirectoryEntry (consulte la tabla [16),](#table-16-generic-primary-directoryentry-template)que deriva de la plantilla Generic DirectoryEntry (vea [la sección 6.2).](#62-generic-directoryentry-template)

<div id="table-16-generic-primary-directoryentry-template" />

**Tabla 16 Directorio principal genérico TemplateEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#631-entrytype-field">la sección 6.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#632-secondarycount-field">la sección 6.3.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#633-setchecksum-field">la sección 6.3.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#634-generalprimaryflags-field">la sección 6.3.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla definen su contenido.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#635-firstcluster-field">la sección 6.3.5</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#636-datalength-field">la sección 6.3.6</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1).](#621-entrytype-field)

##### <a name="6311-typecode-field"></a>6.3.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.1).](#6211-typecode-field)

##### <a name="6312-typeimportance-field"></a>6.3.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.2).](#6212-typeimportance-field)

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 Entradas críticas del directorio principal

Las entradas críticas del directorio principal contienen información que es fundamental para la administración adecuada de un volumen ex RAID. Solo el directorio raíz contiene entradas críticas del directorio principal (las entradas de directorio de archivo son una excepción, vea [la sección 7.4).](#74-file-directory-entry)

La definición de las entradas críticas del directorio principal se correlaciona con el número de revisión ex LDAP principal. Las implementaciones deben admitir todas las entradas críticas del directorio principal y solo registrarán las estructuras de entrada de directorio principal críticas que define esta especificación.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 Entradas de directorio principal benigno

Las entradas del directorio principal benigno contienen información adicional que puede ser útil para administrar un volumen ex EX EX. Cualquier directorio puede contener entradas de directorio principal benignas.

La definición de entradas de directorio principal benignas se correlaciona con el número de revisión ex LDAP menor. La compatibilidad con cualquier entrada de directorio principal benigna que defina esta especificación o cualquier especificación posterior es opcional. Una entrada de directorio principal benigna no reconocida representa todo el conjunto de entradas de directorio como desconocido (más allá de la definición de las plantillas de entrada de directorio aplicables).

##### <a name="6313-typecategory-field"></a>6.3.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.3).](#6213-typecategory-field)

Para esta plantilla, el valor válido para este campo será 0.

##### <a name="6314-inuse-field"></a>6.3.1.4 Campo InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.4).](#6214-inuse-field)

#### <a name="632-secondarycount-field"></a>6.3.2 Campo SecondaryCount

El campo SecondaryCount describirá el número de entradas de directorio secundario que siguen inmediatamente a la entrada de directorio principal dada. Estas entradas de directorio secundario, junto con la entrada de directorio principal dada, componen el conjunto de entradas del directorio.

El intervalo válido de valores para este campo debe ser:

- Al menos 0, lo que significa que esta entrada del directorio principal es la única entrada del conjunto de entradas del directorio.

- Como máximo 255, lo que significa que las siguientes 255 entradas de directorio y esta entrada del directorio principal componen el conjunto de entradas del directorio.

Las estructuras de entrada de directorio principal críticas que derivan de esta plantilla pueden redefinir los campos SecondaryCount y SetChecksum.

#### <a name="633-setchecksum-field"></a>6.3.3 Campo SetChecksum

El campo SetChecksum debe contener la suma de comprobación de todas las entradas de directorio del conjunto de entradas de directorio especificado. Sin embargo, la suma de comprobación excluye este campo (vea [la figura 2).](#figure-2-entrysetchecksum-computation) Las implementaciones comprobarán que el contenido de este campo es válido antes de usar cualquier otra entrada de directorio en el conjunto de entradas de directorio especificado.

Las estructuras de entrada de directorio principal críticas que derivan de esta plantilla pueden redefinir los campos SecondaryCount y SetChecksum.

<div id="figure-2-entrysetchecksum-computation" />

**Figura 2 Cálculo EntrySetChecksum**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>6.3.4 Campo GeneralPrimaryFlags

El campo GeneralPrimaryFlags contiene marcas (consulte [la tabla 17).](#table-17-generic-generalprimaryflags-field-structure)

Las estructuras de entrada de directorio principal críticas que derivan de esta plantilla pueden volver a definir este campo.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabla 17 General genéricoEstado de campoPrimaryFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6341-allocationpossible-field">la sección 6.3.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>No Quechain</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6342-nofatchain-field">la sección 6.3.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla pueden definir este campo.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 Campo AllocationPossible

El campo AllocationPossible debe describir si es posible o no una asignación en el montón de clúster para la entrada de directorio determinada.

Los valores válidos para este campo deben ser:

- 0, lo que significa que no es posible una asignación asociada de clústeres y que los campos FirstCluster y DataLength son realmente indefinidos (las estructuras que derivan de esta plantilla pueden volver a definir esos campos).

- 1, lo que significa que es posible una asignación asociada de clústeres y que los campos FirstCluster y DataLength están definidos.

##### <a name="6342-nofatchain-field"></a>6.3.4.2 Campo NoCompáin

El campo NoAturaChain debe indicar si el FAT activo describe o no la cadena de clúster de la asignación dada.

Los valores válidos para este campo deben ser:

- 0, lo que significa que las entradas FAT correspondientes para la cadena de clúster de la asignación son válidas y las implementaciones las interpretarán; si el campo AllocationPossible contiene el valor 0, o si el campo AllocationPossible contiene el valor 1 y el campo FirstCluster contiene el valor 0, el único valor válido de este campo es 0.

- 1, lo que significa que la asignación asociada es una serie contigua de clústeres; las entradas FAT correspondientes para los clústeres no son válidas y las implementaciones no las interpretarán; Las implementaciones pueden usar la ecuación siguiente para calcular el tamaño de la asignación asociada: DataLength/ (2<sup>SectoresPerClusterShift</sup> \* 2<sup>BytesPerSectorShift)</sup>redondeado al entero más cercano

Si las estructuras de entrada de directorio principal críticas que derivan de esta plantilla redefinen el campo GeneralPrimaryFlags, las entradas FAT correspondientes para cualquier cadena de clúster de asignación asociada son válidas.

#### <a name="635-firstcluster-field"></a>6.3.5 Campo FirstCluster

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.2).](#622-firstcluster-field)

Si el bit NoApiChain es 1, FirstCluster debe apuntar a un clúster válido en el montón del clúster.

Las estructuras de entrada de directorio principal críticas que derivan de esta plantilla pueden redefinir los campos FirstCluster y DataLength. Otras estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DataLength solo si el campo AllocationPossible contiene el valor 0.

#### <a name="636-datalength-field"></a>6.3.6 Campo DataLength

El campo DataLength se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.3).](#623-datalength-field)

Si el bit NoImaChain es 1, DataLength no debe ser cero. Si el campo FirstCluster es cero, DataLength también debe ser cero.

Las estructuras de entrada de directorio principal críticas que derivan de esta plantilla pueden redefinir los campos FirstCluster y DataLength. Otras estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DataLength solo si el campo AllocationPossible contiene el valor 0.

### <a name="64-generic-secondary-directoryentry-template"></a>6.4 Directorio secundario genérico TemplateEntry

El propósito central de las entradas del directorio secundario es proporcionar información adicional sobre un conjunto de entradas de directorio. La capacidad de interpretar la plantilla Generic Secondary DirectoryEntry es obligatoria.

La definición de las entradas del directorio secundario crítico e benigno se correlaciona con el número de revisión exLAC menor. La compatibilidad con cualquier entrada de directorio secundario crítica o benigna que defina esta especificación o especificaciones posteriores es opcional.

Todas las estructuras de entrada de directorio secundario derivan de la plantilla Generic Secondary DirectoryEntry (vea la tabla [18),](#table-18-generic-secondary-directoryentry-template)que deriva de la plantilla Generic DirectoryEntry (vea [la sección 6.2).](#62-generic-directoryentry-template)

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabla 18 Directorio secundario genérico TemplateEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la sección <a href="#641-entrytype-field">6.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#642-generalsecondaryflags-field">la sección 6.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla definen su contenido.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#643-firstcluster-field">la sección 6.4.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#644-datalength-field">la sección 6.4.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1)](#621-entrytype-field)

##### <a name="6411-typecode-field"></a>Campo TypeCode 6.4.1.1

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.1).](#6211-typecode-field)

##### <a name="6412-typeimportance-field"></a>6.4.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.2).](#6212-typeimportance-field)

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 Entradas críticas de directorio secundario

Las entradas críticas del directorio secundario contienen información que es fundamental para la administración adecuada de su conjunto de entradas de directorio que lo contiene.
Aunque la compatibilidad con cualquier entrada de directorio secundario crítica específica es opcional, una entrada de directorio crítica no reconocida representa la entrada de directorio completa establecida como no reconocida (más allá de la definición de las plantillas de entrada de directorio aplicables).

Sin embargo, si un conjunto de entradas de directorio contiene al menos una entrada de directorio secundario crítica que una implementación no reconoce, la implementación interpretará como máximo las plantillas de las entradas de directorio en el conjunto de entradas de directorio y no los datos que ninguna asignación asociada a ninguna entrada de directorio del conjunto de entradas de directorio contiene (Las entradas de directorio de archivo son una excepción, vea la sección [7.4).](#74-file-directory-entry)

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 Entradas de directorio secundario benignas

Las entradas de directorio secundario benignas contienen información adicional que puede ser útil para administrar su conjunto de entradas de directorio que lo contiene. La compatibilidad con cualquier entrada de directorio secundario benigna específica es opcional.
Las entradas de directorio secundario benignas no reconocidas no representan todo el conjunto de entradas de directorio como no reconocidas.

Las implementaciones pueden omitir cualquier entrada secundaria benigna que no reconozca.

##### <a name="6413-typecategory-field"></a>6.4.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.3).](#6213-typecategory-field)

Para esta plantilla, el valor válido para este campo es 1.

##### <a name="6414-inuse-field"></a>Campo 6.4.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.1.4).](#6214-inuse-field)

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 GeneralSecondaryFlags (Campo)

El campo GeneralSecondaryFlags contiene marcas (vea [la tabla 19).](#table-19-generic-generalsecondaryflags-field-structure)

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabla 19 Generic GeneralSecondaryFlags (Estructura de campo)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6421-allocationpossible-field">la sección 6.4.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>NoCompraChain</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#6422-nofatchain-field">la sección 6.4.2.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla pueden definir este campo.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 Campo AllocationPossible

El campo AllocationPossible debe tener la misma definición que el campo con el mismo nombre en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.4.1).](#6341-allocationpossible-field)

##### <a name="6422-nofatchain-field"></a>6.4.2.2 Campo NoCompchain

El campo NoCompChain debe tener la misma definición que el campo con el mismo nombre en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.4.2).](#6342-nofatchain-field)

#### <a name="643-firstcluster-field"></a>6.4.3 Campo FirstCluster

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.2).](#622-firstcluster-field)

Si el bit NoCompChain es 1, FirstCluster debe apuntar a un clúster válido en el montón del clúster.

#### <a name="644-datalength-field"></a>6.4.4 Campo DataLength

El campo DataLength se ajustará a la definición proporcionada en la plantilla Generic DirectoryEntry (consulte [la sección 6.2.3).](#623-datalength-field)

Si el bit NoCompChain es 1, DataLength no debe ser cero. Si el campo FirstCluster es cero, DataLength también debe ser cero.

## <a name="7-directory-entry-definitions"></a>7 Definiciones de entrada de directorio

La revisión 1.00 del sistema de archivos ex LDAP define las siguientes entradas de directorio:

- Principal crítica

  - Mapa de bits de asignación ([sección 7.1](#71-allocation-bitmap-directory-entry))

  - Up-case Table ([Sección 7.2](#72-up-case-table-directory-entry))

  - Etiqueta de volumen ([sección 7.3](#73-volume-label-directory-entry))

  - Archivo ([sección 7.4](#74-file-directory-entry))

- Principal benigna

  - GUID de volumen ([sección 7.5](#75-volume-guid-directory-entry))

  - Relleno De Texas UNOSI ([Sección 7.10](#710-texfat-padding-directory-entry))

<!-- -->

- Secundaria crítica

  - Extensión de stream ([sección 7.6](#76-stream-extension-directory-entry))

  - Nombre de archivo ([sección 7.7](#77-file-name-directory-entry))

- Secundaria benigna

  - Extensión de proveedor ([sección 7.8](#78-vendor-extension-directory-entry))

  - Asignación de proveedores ([sección 7.9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7.1 Entrada de directorio de mapa de bits de asignación

En el sistema de archivos ex FAT, fat no describe el estado de asignación de los clústeres; en su lugar, lo hace un mapa de bits de asignación. Los mapas de bits de asignación existen en el montón de clúster (consulte la sección [7.1.5)](#715-allocation-bitmap)y tienen las entradas de directorio principal críticas correspondientes en el directorio raíz (vea la tabla [20).](#table-20-allocation-bitmap-directoryentry-structure)

El campo NumberOfPlants determina el número de entradas de directorio de mapa de bits de asignación válidas en el directorio raíz. Si el campo NumberOfPlants contiene el valor 1, el único número válido de entradas del directorio Mapa de bits de asignación es 1. Además, la única entrada del directorio Mapa de bits de asignación solo es válida si describe el primer mapa de bits de asignación (vea la sección [7.1.2.1).](#7121-bitmapidentifier-field) Si el campo NumberOfPlants contiene el valor 2, el único número válido de entradas del directorio Mapa de bits de asignación es 2.
Además, las dos entradas del directorio Mapa de bits de asignación solo son válidas si una describe el mapa de bits de primera asignación y la otra describe el segundo mapa de bits de asignación.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabla 20 Allocation Bitmap DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#711-entrytype-field">la sección 7.1.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#712-bitmapflags-field">la sección 7.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>2</td>
<td>18</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#713-firstcluster-field">la sección 7.1.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#714-datalength-field">la sección 7.1.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1).](#631-entrytype-field)

##### <a name="7111-typecode-field"></a>7.1.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.1).](#6311-typecode-field)

Para una entrada del directorio Mapa de bits de asignación, el valor válido para este campo es 1.

##### <a name="7112-typeimportance-field"></a>7.1.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.2).](#6312-typeimportance-field)

Para una entrada del directorio Mapa de bits de asignación, el valor válido para este campo es 0.

##### <a name="7113-typecategory-field"></a>7.1.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.3).](#6313-typecategory-field)

##### <a name="7114-inuse-field"></a>Campo 7.1.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.1.4).](#6314-inuse-field)

#### <a name="712-bitmapflags-field"></a>7.1.2 Campo BitmapFlags

El campo BitmapFlags contiene marcas (vea [tabla 21).](#table-21-bitmapflags-field-structure)

<div id="table-21-bitmapflags-field-structure" />

**Tabla 21 BitmapFlags (estructura de campo)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#7121-bitmapidentifier-field">la sección 7.1.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>1</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 Campo BitmapIdentifier

El campo BitmapIdentifier debe indicar qué mapa de bits de asignación describe la entrada de directorio dada. Las implementaciones deben usar el primer mapa de bits de asignación junto con la primera FAT y usarán el segundo mapa de bits de asignación junto con el segundo FAT. El campo ActiveAtura describe qué FAT y Mapa de bits de asignación están activos.

Los valores válidos para este campo deben ser:

- 0, lo que significa que la entrada de directorio dada describe el primer mapa de bits de asignación

- 1, lo que significa que la entrada de directorio dada describe el segundo mapa de bits de asignación y solo es posible cuando NumberOfPlants contiene el valor 2.

#### <a name="713-firstcluster-field"></a>7.1.3 FirstCluster Field

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.5).](#635-firstcluster-field)

Este campo contiene el índice del primer clúster de la cadena de clúster, como describe FAT, que hospeda el mapa de bits de asignación.

#### <a name="714-datalength-field"></a>7.1.4 Campo DataLength

El campo DataCluster se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.6).](#636-datalength-field)

#### <a name="715-allocation-bitmap"></a>7.1.5 Mapa de bits de asignación

Un mapa de bits de asignación registra el estado de asignación de los clústeres en el montón de clústeres. Cada bit de un mapa de bits de asignación indica si su clúster correspondiente está disponible para la asignación o no.

Un mapa de bits de asignación representa los clústeres del índice más bajo al más alto (consulte [la tabla 22).](#table-22-allocation-bitmap-structure) Por motivos históricos, el primer clúster tiene el índice 2.
Nota: el primer bit del mapa de bits es el bit de orden más bajo del primer byte.

<div id="table-22-allocation-bitmap-structure" />

**Estructura de mapa de bits de asignación de tabla 22**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry[2]</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la sección <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">7.1.5.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry[ClusterCount+1]</td>
<td>ClusterCount : 1</td>
<td>1</td>
<td><p>Este campo es obligatorio y <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">la sección 7.1.5.1</a> define su contenido.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>ClusterCount</td>
<td>(DataLength * 8): ClusterCount</td>
<td><p>Este campo es obligatorio y su contenido, si existe, está reservado.</p>
<p>Nota: Los sectores principal y de arranque de copia de seguridad contienen el campo ClusterCount.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... BitmapEntry \[ ClusterCount+1 \] Fields

Cada campo BitmapEntry de esta matriz representa un clúster en el montón de clústeres. BitmapEntry 2 representa el primer clúster del montón de clústeres y \[ \] BitmapEntry ClusterCount+1 representa el último \[ clúster del montón de \] clústeres.

Los valores válidos para estos campos deben ser:

- 0, que describe el clúster correspondiente como disponible para la asignación

- 1, que describe el clúster correspondiente como no disponible para la asignación (una asignación de clúster ya puede consumir el clúster correspondiente o la FAT activa puede describir el clúster correspondiente como malo)

### <a name="72-up-case-table-directory-entry"></a>7.2 Entrada de directorio de tabla en mayúsculas

La tabla de mayúsculas define la conversión de caracteres en minúsculas a mayúsculas. Esto es importante debido a que la entrada del directorio Nombre de archivo (consulte la sección 7.7) con caracteres Unicode y el sistema de archivos ex LDAP no tiene en cuenta las mayúsculas y minúsculas y la conservación de mayúsculas y minúsculas. La tabla up-case existe en el montón de clústeres (consulte la sección [7.2.5)](#725-up-case-table)y tiene una entrada de directorio principal crítica correspondiente en el directorio raíz (consulte la tabla [23).](#table-23-up-case-table-directoryentry-structure) El número válido de entradas del directorio Up-case Table es 1.

Debido a la relación entre la tabla de mayúsculas y los nombres de archivo, las implementaciones no deben modificar la tabla de mayúsculas y minúsculas, excepto como resultado de las operaciones de formato.

<div id="table-23-up-case-table-directoryentry-structure" />

**Table 23 Up-case Table DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#721-entrytype-field">la sección 7.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#722-tablechecksum-field">la sección 7.2.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#723-firstcluster-field">la sección 7.2.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#724-datalength-field">la sección 7.2.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1).](#631-entrytype-field)

##### <a name="7211-typecode-field"></a>7.2.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.1).](#6311-typecode-field)

Para la entrada del directorio Up-case Table, el valor válido para este campo es
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.2).](#6312-typeimportance-field)

Para la entrada del directorio Up-case Table, el valor válido para este campo es
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.3).](#6313-typecategory-field)

##### <a name="7214-inuse-field"></a>7.2.1.4 Campo InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.1.4).](#6314-inuse-field)

#### <a name="722-tablechecksum-field"></a>7.2.2 Campo TableChecksum

El campo TableChecksum contiene la suma de comprobación de la tabla up-case (que describen los campos FirstCluster y DataLength). Las implementaciones comprobarán que el contenido de este campo es válido antes de usar la tabla up-case.

<div id="figure-3-tablechecksum-computation" />

**Figura 3 Cálculo de TableChecksum**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 FirstCluster Field

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.5).](#635-firstcluster-field)

Este campo contiene el índice del primer clúster de la cadena de clústeres, como describe FAT, que hospeda la tabla up-case.

#### <a name="724-datalength-field"></a>7.2.4 Campo DataLength

El campo DataCluster se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.6).](#636-datalength-field)

#### <a name="725-up-case-table"></a>7.2.5 Tabla de mayúsculas y minúsculas

Una tabla de mayúsculas y minúsculas es una serie de asignaciones de caracteres Unicode. Una asignación de caracteres consta de un campo de 2 bytes, con el índice del campo en la tabla de mayúsculas y minúsculas que representa el carácter Unicode al que se va a usar mayúsculas y minúsculas, y el campo de 2 bytes que representa el carácter Unicode con mayúsculas y minúsculas.

Los primeros 128 caracteres Unicode tienen asignaciones obligatorias (vea [la tabla 24).](#table-24-mandatory-first-128-up-case-table-entries)
Una tabla de mayúsculas y minúsculas que tiene cualquier otra asignación de caracteres para cualquiera de los primeros 128 caracteres Unicode no es válida.

Las implementaciones que solo admiten caracteres del intervalo de asignación obligatorio pueden omitir las asignaciones del resto de la tabla de mayúsculas y minúsculas. Estas implementaciones solo deben usar caracteres del intervalo de asignación obligatorio al crear o cambiar el nombre de los archivos (a través de la entrada del directorio Nombre de archivo, consulte [la sección 7.7).](#77-file-name-directory-entry) Al aplicar mayúsculas y minúsculas a los nombres de archivo existentes, estas implementaciones no deben mostrar caracteres de mayúsculas y minúsculas del intervalo de asignación no obligatorio, pero deben dejarlos intactos en el nombre de archivo con mayúsculas y minúsculas resultante (se trata de un uso parcial de mayúsculas y minúsculas). Al comparar nombres de archivo, estas implementaciones deben tratar los nombres de archivo que difieren del nombre en comparación solo por caracteres Unicode del intervalo de asignación no obligatorio como equivalentes. Aunque estos nombres de archivo solo son potencialmente equivalentes, estas implementaciones no pueden garantizar que el nombre de archivo con mayúsculas y minúsculas no entre en colisión con el nombre en comparación.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabla 24 Primeras 128 entradas de tabla de mayúsculas y minúsculas obligatorias**

| Índice de tabla | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000 Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004 Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005 Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004 Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(Nota: Las entradas con asignaciones de mayúsculas y minúsculas que no son de identidad están en negrita)**

Al dar formato a un volumen, las implementaciones pueden generar una tabla de mayúsculas y minúsculas en un formato comprimido mediante la compresión de asignación de identidad, ya que una gran parte del espacio de caracteres Unicode no tiene ningún concepto de mayúsculas y minúsculas (lo que significa que los caracteres "en minúsculas" y "mayúsculas" son equivalentes).
Las implementaciones comprimen una tabla de mayúsculas y minúsculas mediante la representación de una serie de asignaciones de identidad con el valor FFFFh seguido del número de asignaciones de identidad.

Por ejemplo, una implementación puede representar las primeras asignaciones de caracteres de 100 (64 h) con las ocho entradas siguientes de una tabla de mayúsculas y minúsculas comprimida:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Las dos primeras entradas indican que los primeros 97 caracteres (61h) (de 0000h a 0060h) tienen asignaciones de identidad. Los caracteres siguientes, de 0061h a 0063h, se asignan a caracteres de 0041h a 0043h, respectivamente.

La capacidad de proporcionar una tabla de mayúsculas y minúsculas comprimida al dar formato a un volumen es opcional. Sin embargo, es obligatoria la capacidad de interpretar una tabla de mayúsculas y minúsculas sin comprimir. El valor del campo TableChecksum siempre se ajusta a cómo existe la tabla de mayúsculas y minúsculas en el volumen, que puede estar en formato comprimido o sin comprimir.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 Tabla de mayúsculas y minúsculas recomendada

Al dar formato a un volumen, las implementaciones deben registrar la tabla de mayúsculas y minúsculas recomendada en formato comprimido (vea tabla [25),](#table-25-recommended-up-case-table-in-compressed-format)para el que el valor del campo TableChecksum es E619D30Dh.

Si una implementación define su propia tabla de mayúsculas y minúsculas, ya sea comprimida o sin comprimir, esa tabla cubrirá el intervalo de caracteres Unicode completo (de códigos de caracteres 0000h a FFFFh inclusive).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabla 25 Tabla de mayúsculas y minúsculas recomendada en formato comprimido**

| Desplazamiento sin procesar | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000 Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004 Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005 Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004 Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027 Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02BBh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035 Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040 Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041 Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040 Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04 A0h**      | 04 A0h                        | 04 A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054 Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055 Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054 Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFh   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06 A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07 A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200ah   | 200 Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201 Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022 h   | 2023h   |
| **0830h**      | 2024 h                        | 2025 h   | 2026 h   | 2027 h   | 2028 h   | 2029h   | 202Ah   | 202 Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032 h   | 2033 h   |
| **0840h**      | 2034 h                        | 2035h   | 2036 h   | 2037 h   | 2038 h   | 2039h   | 203Ah   | 203 Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041 h   | 2042 h   | 2043 h   |
| **0850h**      | 2044 h                        | 2045 h   | 2046 h   | 2047 h   | 2048 h   | 2049h   | 204Ah   | 204 Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052 h   | 2053h   |
| **0860h**      | 2054h                        | 2055 h   | 2056 h   | 2057h   | 2058 h   | 2059h   | 205Ah   | 205 Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061 h   | 2062 h   | 2063 h   |
| **0870h**      | 2064 h                        | 2065 h   | 2066 h   | 2067 h   | 2068 h   | 2069h   | 206Ah   | 206 Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071 h   | 2072 h   | 2073 h   |
| **0880h**      | 2074 h                        | 2075 h   | 2076 h   | 2077 h   | 2078 h   | 2079h   | 207Ah   | 207 Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081 h   | 2082 h   | 2083 h   |
| **0890h**      | 2084 h                        | 2085 h   | 2086 h   | 2087 h   | 2088 h   | 2089h   | 208Ah   | 208 Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091 h   | 2092h   | 2093h   |
| **08A0h**      | 2094 h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20 A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100 h   | 2101 h   | 2102 h   | 2103 h   |
| **0910h**      | 2104 h                        | 2105 h   | 2106 h   | 2107 h   | 2108 h   | 2109h   | 210Ah   | 210 Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115 h   | 2116 h   | 2117 h   | 2118 h   | 2119h   | 211Ah   | 211 Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120 h   | 2121 h   | 2122 h   | 2123 h   |
| **0930h**      | 2124 h                        | 2125 h   | 2126 h   | 2127 h   | 2128 h   | 2129 h   | 212Ah   | 212 Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130 h   | 2131 h   | 2132 h   | 2133 h   |
| **0940h**      | 2134 h                        | 2135 h   | 2136 h   | 2137 h   | 2138 h   | 2139 h   | 213 Días   | 213 Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140 h   | 2141 h   | 2142 h   | 2143 h   |
| **0950h**      | 2144 h                        | 2145 h   | 2146 h   | 2147 h   | 2148 h   | 2149 h   | 214Ah   | 214 Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132 h   | 214Fh   | 2150 h   | 2151 h   | 2152 h   | 2153 h   |
| **0960h**      | 2154 h                        | 2155 h   | 2156 h   | 2157 h   | 2158 h   | 2159h   | 215 Días   | 215 Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160 h   | 2161 h   | 2162 h   | 2163 h   |
| **0970h**      | 2164 h                        | 2165 h   | 2166 h   | 2167 h   | 2168 h   | 2169 h   | 216Ah   | 216 Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160 h   | 2161 h   | 2162 h   | 2163 h   |
| **0980h**      | 2164 h                        | 2165 h   | 2166 h   | 2167 h   | 2168 h   | 2169 h   | 216Ah   | 216 Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180 h   | 2181 h   | 2182 h   | 2183 h   |
| **0990h**      | 2183 h                        | FFFFh   | 034 Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24 BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09 A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10 A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10BBh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7.3 Entrada de directorio de etiquetas de volumen

La etiqueta de volumen es una cadena Unicode que permite a los usuarios finales distinguir sus volúmenes de almacenamiento. En el sistema de archivos ex RAID, la etiqueta de volumen existe como una entrada de directorio principal crítica en el directorio raíz (consulte [la tabla 26).](#table-26-volume-label-directoryentry-structure) El número válido de entradas de directorio de etiquetas de volumen va de 0 a 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabla 26 Volume Label DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#731-entrytype-field">la sección 7.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#732-charactercount-field">la sección 7.3.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Este campo es obligatorio y <a href="#733-volumelabel-field">la sección 7.3.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1).](#631-entrytype-field)

##### <a name="7311-typecode-field"></a>7.3.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.1).](#6311-typecode-field)

Para la entrada del directorio Etiqueta de volumen, el valor válido para este campo es
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.2).](#6312-typeimportance-field)

Para la entrada del directorio Etiqueta de volumen, el valor válido para este campo es
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.3).](#6313-typecategory-field)

##### <a name="7314-inuse-field"></a>Campo 7.3.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.1.4).](#6314-inuse-field)

#### <a name="732-charactercount-field"></a>7.3.2 Campo CharacterCount

El campo CharacterCount debe contener la longitud de la cadena Unicode que contiene el campo VolumeLabel.

El intervalo válido de valores para este campo debe ser:

- Al menos 0, lo que significa que la cadena Unicode tiene 0 caracteres de longitud (que es el equivalente de ninguna etiqueta de volumen)

- Como máximo 11, lo que significa que la cadena Unicode tiene 11 caracteres de longitud

#### <a name="733-volumelabel-field"></a>7.3.3 Campo VolumeLabel

El campo VolumeLabel debe contener una cadena Unicode, que es el nombre descriptivo del volumen. El campo VolumeLabel tiene el mismo conjunto de caracteres no válidos que el campo FileName de la entrada del directorio Nombre de archivo (consulte la sección [7.7.3).](#773-filename-field)

### <a name="74-file-directory-entry"></a>7.4 Entrada del directorio de archivos

Las entradas del directorio de archivos describen archivos y directorios. Son entradas de directorio principal críticas y cualquier directorio puede contener cero o más entradas de directorio de archivo (consulte [la tabla 27).](#table-27-file-directoryentry) Para que una entrada de directorio de archivo sea válida, exactamente una entrada de directorio de extensión de flujo y al menos una entrada de directorio nombre de archivo deben seguir inmediatamente la entrada del directorio Archivo (consulte las secciones [7.6](#76-stream-extension-directory-entry) y [7.7,](#77-file-name-directory-entry)respectivamente).

<div id="table-27-file-directoryentry" />

**Tabla 27 File DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#741-entrytype-field">la sección 7.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#742-secondarycount-field">la sección 7.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#743-setchecksum-field">la sección 7.4.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#744-fileattributes-field">la sección 7.4.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sección 7.4.5 </
a> define su contenido.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">la sección 7.4.6</a> define su contenido.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">la sección 7.4.7</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sección 7.4.5 </
a> define su contenido.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">la sección 7.4.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sección 7.4.5 </
a> define su contenido.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">la sección 7.4.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">la sección 7.4.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1).](#631-entrytype-field)

##### <a name="7411-typecode-field"></a>7.4.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.1).](#6311-typecode-field)

Para una entrada de directorio de archivo, el valor válido para este campo es 5.

##### <a name="7412-typeimportance-field"></a>7.4.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.2).](#6312-typeimportance-field)

Para una entrada de directorio de archivo, el valor válido para este campo es 0.

##### <a name="7413-typecategory-field"></a>7.4.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.3).](#6313-typecategory-field)

##### <a name="7414-inuse-field"></a>Campo 7.4.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.1.4).](#6314-inuse-field)

#### <a name="742-secondarycount-field"></a>7.4.2 Campo SecondaryCount

El campo SecondaryCount se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.2).](#632-secondarycount-field)

#### <a name="743-setchecksum-field"></a>7.4.3 Campo SetChecksum

El campo SetChecksum se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.3).](#633-setchecksum-field)

#### <a name="744-fileattributes-field"></a>7.4.4 Campo FileAttributes

El campo FileAttributes contiene marcas (vea [la tabla 28).](#table-28-fileattributes-field-structure)

<div id="table-28-fileattributes-field-structure" />

**Estructura de campo FileAttributes de tabla 28**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y se ajusta a la definición de MS-DOS.</td>
</tr>
<tr class="even">
<td>Hidden</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y se ajusta a la definición de MS-DOS.</td>
</tr>
<tr class="odd">
<td>Sistema</td>
<td>2</td>
<td>1</td>
<td>Este campo es obligatorio y se ajusta a la definición de MS-DOS.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="odd">
<td>Directorio</td>
<td>4</td>
<td>1</td>
<td>Este campo es obligatorio y se ajusta a la definición de MS-DOS.</td>
</tr>
<tr class="even">
<td>Archivo</td>
<td>5</td>
<td>1</td>
<td>Este campo es obligatorio y se ajusta a la definición de MS-DOS.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>7.4.5 CreateTimestamp, Create10msIncrement y CreateUtcOffset Fields

En combinación, los campos CreateTimestamp y CreateTime10msIncrement deberán describir la fecha y hora locales en que se creó el archivo o directorio especificado. El campo CreateUtcOffset describe el desplazamiento de la fecha y hora locales con respecto a la hora UTC. Las implementaciones deben establecer estos campos tras la creación del conjunto de entrada de directorio especificado.

Estos campos se ajustarán a las definiciones de los campos Timestamp, 10msIncrement y UtcOffset (vea sección [7.4.8,](#748-timestamp-fields)sección [7.4.9](#749-10msincrement-fields)y sección [7.4.10,](#7410-utcoffset-fields)respectivamente).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>7.4.6 Campos LastModifiedTimestamp, LastModified10msIncrement y LastModifiedUtcOffset

En combinación, los campos LastModifiedTimestamp y LastModifiedTime10msIncrement deberán describir la fecha y hora locales en que se modificó por última vez el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de flujo especificada. El campo LastModifiedUtcOffset describe el desplazamiento de la fecha y hora locales con respecto a la hora UTC. Las implementaciones actualizarán estos campos:

1. Después de modificar el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia dada (excepto para el contenido que existe más allá del punto que describe el campo ValidDataLength)

2. Al cambiar los valores de los campos ValidDataLength o DataLength

Estos campos se ajustarán a las definiciones de los campos Timestamp, 10msIncrement y UtcOffset (vea sección [7.4.8,](#748-timestamp-fields)sección [7.4.9](#749-10msincrement-fields)y sección [7.4.10,](#7410-utcoffset-fields)respectivamente).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 Campos LastAccessedTimestamp y LastAccessedUtcOffset

El campo LastAccessedTimestamp debe describir la fecha y hora locales en que se ha accedido por última vez al contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia especificada. El campo LastAccessedUtcOffset describe el desplazamiento de la fecha y hora locales con respecto a la hora UTC.
Las implementaciones actualizarán estos campos:

1. Después de modificar el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia dada (excepto para el contenido que existe más allá de ValidDataLength)

2. Al cambiar los valores de los campos ValidDataLength o DataLength

Las implementaciones deben actualizar estos campos después de leer el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia dada.

Estos campos se ajustarán a las definiciones de los campos Timestamp y UtcOffset (consulte las secciones [7.4.8](#748-timestamp-fields) y [7.4.10,](#7410-utcoffset-fields)respectivamente).

#### <a name="748-timestamp-fields"></a>7.4.8 Campos de marca de tiempo

Los campos de marca de tiempo describen la fecha y hora locales, hasta una resolución de dos segundos (consulte [la tabla 29).](#table-29-timestamp-field-structure)

<div id="table-29-timestamp-field-structure" />

**Estructura de campo de marca de tiempo de tabla 29**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Este campo es obligatorio y <a href="#7481-doubleseconds-field">la sección 7.4.8.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Minuto</td>
<td>5</td>
<td>6</td>
<td>Este campo es obligatorio y <a href="#7482-minute-field">la sección 7.4.8.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Hora</td>
<td>11</td>
<td>5</td>
<td>Este campo es obligatorio y <a href="#7483-hour-field">la sección 7.4.8.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Día</td>
<td>16</td>
<td>5</td>
<td>Este campo es obligatorio y <a href="#7484-day-field">la sección 7.4.8.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Month (Mes)</td>
<td>21</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#7485-month-field">la sección 7.4.8.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Este campo es obligatorio y <a href="#7486-year-field">la sección 7.4.8.6</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>Campo DoubleSeconds de 7.4.8.1

El campo DoubleSeconds describirá la parte de segundos del campo Timestamp, en múltiplo de dos segundos.

El intervalo válido de valores para este campo debe ser:

- 0, que representa 0 segundos

- 29, que representa 58 segundos

##### <a name="7482-minute-field"></a>Campo 7.4.8.2 Minute

El campo Minuto describirá la parte de minutos del campo Marca de tiempo.

El intervalo válido de valores para este campo debe ser:

- 0, que representa 0 minutos

- 59, que representa 59 minutos

##### <a name="7483-hour-field"></a>Campo hora 7.4.8.3

El campo Hora describirá la parte de horas del campo Marca de tiempo.

El intervalo válido de valores para este campo debe ser:

- 0, que representa las 00:00 horas

- 23, que representa las 23:00 horas

##### <a name="7484-day-field"></a>Campo 7.4.8.4 Day

El campo Día describirá la parte del día del campo Marca de tiempo.

El intervalo válido de valores para este campo debe ser:

- 1, que es el primer día del mes dado

- El último día del mes dado (el mes especificado define el número de días válidos)

##### <a name="7485-month-field"></a>Campo 7.4.8.5 Month

El campo Mes describirá la parte del mes del campo Marca de tiempo.

El intervalo válido de valores para este campo debe ser:

- Al menos 1, que representa enero

- Como máximo 12, que representa diciembre

##### <a name="7486-year-field"></a>Campo 7.4.8.6 Año

El campo Año describirá la parte del año del campo Marca de tiempo, en relación con el año 1980. Este campo representa el año 1980 con el valor 0 y el año 2107 con el valor 127.

Todos los valores posibles para este campo son válidos.

#### <a name="749-10msincrement-fields"></a>7.4.9 10 ms Campos de creación

Los campos de 10 msincrement deben proporcionar una resolución de tiempo adicional a sus campos timestamp correspondientes en múltiplo de diez milisegundos.

El intervalo válido de valores para estos campos debe ser:

- Al menos 0, que representa 0 milisegundos

- Como máximo 199, que representa 1990 milisegundos

#### <a name="7410-utcoffset-fields"></a>7.4.10 UtcOffset Fields

Los campos UtcOffset (consulte la tabla [30)](#table-30-utcoffset-field-structure)describen el desplazamiento de UTC a la fecha y hora locales que describen sus campos Timestamp y 10msIncrement correspondientes. El desplazamiento de UTC a la fecha y hora local incluye los efectos de las zonas horarias y otros ajustes de fecha y hora, como el horario de verano y los cambios regionales del horario de verano.

<div id="table-30-utcoffset-field-structure" />

**Tabla 30 UtcOffset (estructura de campos)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bits)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Este campo es obligatorio y <a href="#74101-offsetfromutc-field">la sección 7.4.10.1</a>define su contenido.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#74102-offsetvalid-field">la sección 7.4.10.2</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>Campo OffsetFromUtc 7.4.10.1

El campo OffsetFromUtc debe describir el desplazamiento con respecto a la hora UTC de la fecha y hora locales que contienen los campos Timestamp y 10msIncrement relacionados.
En este campo se describe el desplazamiento de utc en intervalos de 15 minutos (consulte la tabla 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabla 31 Significado de los valores del campo OffsetFromUtc**

<table>
<thead>
<tr class="header">
<th><strong>Valor</strong></th>
<th><strong>Equivalente decimal con signo</strong></th>
<th><strong>Descripción</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>La fecha y hora locales son UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>La fecha y hora locales son UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>La fecha y hora locales son UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00h</td>
<td>0</td>
<td>La fecha y hora locales son UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>La fecha y hora locales son UTC: 00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41h</td>
<td>-63</td>
<td>La fecha y hora locales son UTC: 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>Fecha y hora locales es UTC – 16:00</td>
</tr>
</tbody>
</table>

Como indica la tabla anterior, todos los valores posibles para este campo son válidos. Sin embargo, las implementaciones solo deben registrar el valor 00h para este campo cuando:

1. La fecha y hora locales son realmente las mismas que las UTC, en cuyo caso el valor del campo OffsetValid será 1.

2. No se conoce la fecha y hora locales, en cuyo caso el valor del campo OffsetValid debe ser 1 y las implementaciones deben considerar la hora UTC como fecha y hora locales.

3. Utc no se conoce, en cuyo caso el valor del campo OffsetValid debe ser 0.

Si el desplazamiento de fecha y hora local con respecto a utc no es un múltiplo de intervalos de 15 minutos, las implementaciones registrarán 00h en el campo OffsetFromUtc y considerarán utc como fecha y hora locales.

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 Campo OffsetValid

El campo OffsetValid debe describir si el contenido del campo OffsetFromUtc es válido o no, como se indica a continuación:

- 0, lo que significa que el contenido del campo OffsetFromUtc no es válido
    > y deben ser 00h

- 1, lo que significa que el contenido del campo OffsetFromUtc es válido

Las implementaciones solo deben establecer este campo en el valor 0 cuando UTC no está disponible para calcular el valor del campo OffsetFromUtc. Si este campo contiene el valor 0, las implementaciones deben tratar los campos Timestamp y 10msIncrement como que tienen el mismo desplazamiento UTC que la fecha y hora local actuales.

### <a name="75-volume-guid-directory-entry"></a>7.5 Entrada de directorio GUID de volumen

La entrada del directorio GUID de volumen contiene un GUID que permite a las implementaciones distinguir volúmenes de forma única y mediante programación.
El GUID del volumen existe como una entrada de directorio principal benigno en el directorio raíz (consulte [la tabla 32).](#table-32-volume-guid-directoryentry) El número válido de entradas de directorio GUID de volumen oscila entre 0 y 1.

<div id="table-32-volume-guid-directoryentry" />

**Table 32 Volume GUID DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#751-entrytype-field">la sección 7.5.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#752-secondarycount-field">la sección 7.5.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#753-setchecksum-field">la sección 7.5.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#754-generalprimaryflags-field">la sección 7.5.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#755-volumeguid-field">la sección 7.5.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>22</td>
<td>10</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1).](#631-entrytype-field)

##### <a name="7511-typecode-field"></a>7.5.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.1).](#6311-typecode-field)

Para la entrada del directorio GUID de volumen, el valor válido para este campo es
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.2).](#6312-typeimportance-field)

Para la entrada del directorio GUID de volumen, el valor válido para este campo es
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.3).](#6313-typecategory-field)

##### <a name="7514-inuse-field"></a>Campo 7.5.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.1.4).](#6314-inuse-field)

#### <a name="752-secondarycount-field"></a>7.5.2 Campo SecondaryCount

El campo SecondaryCount se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.2).](#632-secondarycount-field)

Para la entrada del directorio GUID de volumen, el valor válido para este campo es
0.

#### <a name="753-setchecksum-field"></a>7.5.3 Campo SetChecksum

El campo SetChecksum se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.3).](#633-setchecksum-field)

#### <a name="754-generalprimaryflags-field"></a>7.5.4 GeneralPrimaryFlags (Campo)

El campo GeneralPrimaryFlags se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.4)](#634-generalprimaryflags-field)y definirá el contenido del campo CustomDefined que se va a reservar.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 Campo AllocationPossible

El campo AllocationPossible se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte [la sección 6.3.4.1).](#6341-allocationpossible-field)

Para la entrada del directorio GUID de volumen, el valor válido para este campo es
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 Campo NoCompchain

El campo No LdapChain se ajustará a la definición proporcionada en la plantilla Generic Primary DirectoryEntry (consulte la sección [6.3.4.2).](#6342-nofatchain-field)

#### <a name="755-volumeguid-field"></a>7.5.5 Campo VolumeGuid

El campo VolumeGuid debe contener un GUID que identifique de forma única el volumen especificado.

Todos los valores posibles para este campo son válidos, excepto el GUID nulo, que es {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>7.6 Entrada del directorio de extensión de secuencia

La entrada de directorio de la extensión de flujo es una entrada de directorio secundario crítica en conjuntos de entradas de directorio de archivos (consulte [la tabla 33).](#table-33-stream-extension-directoryentry) El número válido de entradas de directorio de la extensión de flujo en un conjunto de entradas de directorio de archivo es 1.
Además, esta entrada de directorio solo es válida si sigue inmediatamente a la entrada Directorio de archivos.

<div id="table-33-stream-extension-directoryentry" />

**Tabla 33 Stream Extension DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#761-entrytype-field">la sección 7.6.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#762-generalsecondaryflags-field">la sección 7.6.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#763-namelength-field">la sección 7.6.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y <a href="#764-namehash-field">la sección 7.6.4</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#765-validdatalength-field">la sección 7.6.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved3</td>
<td>16</td>
<td>4</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#766-firstcluster-field">la sección 7.6.6</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#767-datalength-field">la sección 7.6.7</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1).](#641-entrytype-field)

##### <a name="7611-typecode-field"></a>7.6.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.1).](#6411-typecode-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 0.

##### <a name="7612-typeimportance-field"></a>7.6.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.2).](#6412-typeimportance-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 0.

##### <a name="7613-typecategory-field"></a>7.6.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.3).](#6413-typecategory-field)

##### <a name="7614-inuse-field"></a>Campo 7.6.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.4).](#6414-inuse-field)

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 GeneralSecondaryFlags (Campo)

El campo GeneralSecondaryFlags se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2)](#642-generalsecondaryflags-field)y definirá el contenido del campo CustomDefined que se va a reservar.

##### <a name="7621-allocationpossible-field"></a>7.6.2.1 Campo AllocationPossible

El campo AllocationPossible se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.1).](#6421-allocationpossible-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 1.

##### <a name="7622-nofatchain-field"></a>7.6.2.2 Campo NoCompchain

El campo NoCompChain se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.2).](#6422-nofatchain-field)

#### <a name="763-namelength-field"></a>7.6.3 Campo NameLength

El campo NameLength debe contener la longitud de la cadena Unicode que contienen colectivamente las entradas de directorio de nombre de archivo subsiguientes (consulte la sección [7.7).](#77-file-name-directory-entry)

El intervalo válido de valores para este campo debe ser:

- Al menos 1, que es el nombre de archivo más corto posible

- Como máximo 255, que es el nombre de archivo más largo posible

El valor del campo NameLength también afecta al número de entradas de directorio de nombre de archivo (consulte [la sección 7.7).](#77-file-name-directory-entry)

#### <a name="764-namehash-field"></a>7.6.4 NameHash Field

El campo NameHash debe contener un hash de 2 bytes (consulte la figura [4)](#figure-4-namehash-computation)del nombre de archivo con mayúsculas y minúsculas. Esto permite a las implementaciones realizar una comparación rápida al buscar un archivo por nombre. Lo importante es que NameHash proporciona una comprobación segura de un error de coincidencia. Las implementaciones deben comprobar todas las coincidencias de NameHash con una comparación del nombre de archivo con mayúsculas y minúsculas.

<div id="figure-4-namehash-computation" />

**Figura 4 Cálculo de NameHash**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>7.6.5 Campo ValidDataLength

El campo ValidDataLength debe describir hasta qué punto se han escrito los datos de usuario del flujo de datos. Las implementaciones actualizarán este campo a medida que escriban datos en el flujo de datos. En el medio de almacenamiento, los datos entre la longitud de datos válida y la longitud de datos del flujo de datos no están definidos. Las implementaciones devolverán ceros para las operaciones de lectura más allá de la longitud de datos válida.

Si la entrada del directorio File correspondiente describe un directorio, el único valor válido para este campo es igual al valor del campo DataLength. De lo contrario, el intervalo de valores válidos para este campo será:

- Al menos 0, lo que significa que no se ha escrito ningún dato de usuario en el flujo de datos

- Como máximo DataLength, lo que significa que los datos de usuario se han escrito en toda la longitud del flujo de datos.

#### <a name="766-firstcluster-field"></a>7.6.6 FirstCluster Field

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.3).](#643-firstcluster-field)

Este campo debe contener el índice del primer clúster del flujo de datos, que hospeda los datos del usuario.

#### <a name="767-datalength-field"></a>7.6.7 Campo DataLength

El campo DataLength se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.4).](#644-datalength-field)

Si la entrada del directorio File correspondiente describe un directorio, el valor válido para este campo es el tamaño completo de la asignación asociada, en bytes, que puede ser 0. Además, para los directorios, el valor máximo de este campo es 256 MB.

### <a name="77-file-name-directory-entry"></a>7.7 Entrada de directorio de nombre de archivo

Las entradas de directorio de nombre de archivo son entradas de directorio secundarias críticas en conjuntos de entradas de directorio de archivos (consulte [la tabla 34).](#table-34-file-name-directoryentry) El número válido de entradas del directorio Nombre de archivo en un conjunto de entradas de directorio de archivos es NameLength/15, redondeado al entero más cercano. Además, las entradas del directorio Nombre de archivo solo son válidas si siguen inmediatamente la entrada del directorio de extensión de secuencia como una serie consecutiva. Las entradas del directorio Nombre de archivo se combinan para formar el nombre de archivo del conjunto de entradas directorio de archivo.

Todos los secundarios de una entrada de directorio determinada deben tener conjuntos de entrada de directorio de nombre de archivo únicos. Es decir, no puede haber nombres de archivo o directorio duplicados después de usar mayúsculas y minúsculas en cualquier directorio.

<div id="table-34-file-name-directoryentry" />

**Tabla 34 Nombre de archivo DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#771-entrytype-field">la sección 7.7.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#772-generalsecondaryflags-field">la sección 7.7.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Este campo es obligatorio y <a href="#773-filename-field">la sección 7.7.3</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1).](#641-entrytype-field)

##### <a name="7711-typecode-field"></a>7.7.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.1).](#6411-typecode-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 1.

##### <a name="7712-typeimportance-field"></a>7.7.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.2).](#6412-typeimportance-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 0.

##### <a name="7713-typecategory-field"></a>7.7.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.3).](#6413-typecategory-field)

##### <a name="7714-inuse-field"></a>Campo 7.7.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.4).](#6414-inuse-field)

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 GeneralSecondaryFlags (Campo)

El campo GeneralSecondaryFlags se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2)](#642-generalsecondaryflags-field)y definirá el contenido del campo CustomDefined que se va a reservar.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 Campo AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2.1).](#6421-allocationpossible-field)

Para la entrada de directorio de la extensión de flujo, el valor válido para este campo es 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 Campo NoCompchain

El campo NoCompChain se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.2).](#6422-nofatchain-field)

#### <a name="773-filename-field"></a>7.7.3 Campo FileName

El campo FileName debe contener una cadena Unicode, que es una parte del nombre de archivo. En el orden en que las entradas del directorio Nombre de archivo existen en un conjunto de entradas de directorio de archivos, los campos FileName se concatenan para formar el nombre de archivo del conjunto de entradas directorio de archivo. Dada la longitud del campo FileName, 15 caracteres y el número máximo de entradas de directorio de nombre de archivo, 17, la longitud máxima del nombre de archivo concatenado final es
255.

El nombre de archivo concatenado tiene el mismo conjunto de caracteres no válidos que otros sistemas de archivos basados en FAT (consulte [la tabla 35).](#table-35-invalid-filename-characters) Las implementaciones deben establecer los caracteres no usados de los campos FileName en el valor 0000h.

<div id="table-35-invalid-filename-characters" />

**Tabla 35 Caracteres fileName no válidos**

| **Código de caracteres** | **Descripción** | **Código de caracteres** | **Descripción**   | **Código de caracteres** | **Descripción** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Código de control    | 0001h              | Código de control      | 0002h              | Código de control    |
| 0003h              | Código de control    | 0004h              | Código de control      | 0005h              | Código de control    |
| 0006h              | Código de control    | 0007h              | Código de control      | 0008h              | Código de control    |
| 0009h              | Código de control    | 000Ah              | Código de control      | 000 Bh              | Código de control    |
| 000Ch              | Código de control    | 000Dh              | Código de control      | 000Eh              | Código de control    |
| 000Fh              | Código de control    | 0010h              | Código de control      | 0011h              | Código de control    |
| 0012h              | Código de control    | 0013h              | Código de control      | 0014h              | Código de control    |
| 0015h              | Código de control    | 0016h              | Código de control      | 0017h              | Código de control    |
| 0018h              | Código de control    | 0019h              | Código de control      | 001Ah              | Código de control    |
| 001Bh              | Código de control    | 001Ch              | Código de control      | 001Dh              | Código de control    |
| 001Eh              | Código de control    | 001Fh              | Código de control      | 0022h              | Comillas  |
| 002Ah              | Asterisk        | 002Fh              | Barra diagonal     | 003Ah              | Dos puntos           |
| 003Ch              | Signo de menor que  | 003Eh              | Signo de mayor que | 003Fh              | Signo de interrogación   |
| 005Ch              | Barra diagonal hacia atrás      | 007Ch              | Barra vertical      |                    |                 |

Los nombres de archivo "." y ".." tienen el significado especial de "este directorio" y "directorio que contiene", respectivamente. Las implementaciones no registrarán ninguno de estos nombres de archivo reservados en el campo FileName.
Sin embargo, las implementaciones pueden generar estos dos nombres de archivo en las listas de directorios para hacer referencia al directorio que se muestra y al directorio que lo contiene.

Es posible que las implementaciones de quieran restringir los nombres de archivo y directorio solo al juego de caracteres ASCII. Si es así, deben limitar su uso de caracteres al intervalo de caracteres válidos en las primeras 128 entradas Unicode. Todavía deben almacenar nombres de archivo y directorio en Unicode en el volumen y traducir a o desde ASCII/Unicode al interfacing con el usuario.

### <a name="78-vendor-extension-directory-entry"></a>7.8 Entrada del directorio de extensión de proveedor

La entrada del directorio vendor extension es una entrada de directorio secundario benigna en conjuntos de entradas de directorio de archivos (consulte [la tabla 36).](#table-36-vendor-extension-directoryentry) Un conjunto de entradas de directorio de archivo puede contener cualquier número de entradas de directorio de extensión de proveedor, hasta el límite de entradas de directorio secundario, menos el número de otras entradas de directorio secundario. Además, las entradas de directorio de extensión de proveedor solo son válidas si no preceden a las entradas de directorio extensión de secuencia y nombre de archivo necesarias.

Las entradas de directorio de extensión de proveedor permiten a los proveedores tener entradas de directorio únicas específicas del proveedor en conjuntos de entradas individuales de directorio de archivos a través del campo VendorGuid (consulte la [tabla 36).](#table-36-vendor-extension-directoryentry) Las entradas de directorio únicas permiten a los proveedores ampliar de forma eficaz el sistema de archivos ex LDAP. Los proveedores pueden definir el contenido del campo VendorDefined (Definido por el proveedor) (consulte [la tabla 36).](#table-36-vendor-extension-directoryentry) Las implementaciones de proveedor pueden mantener el contenido del campo VendorDefined y pueden proporcionar funcionalidad específica del proveedor.

Las implementaciones que no reconocen el GUID de una entrada de directorio de extensión de proveedor deben tratar la entrada de directorio igual que cualquier otra entrada de directorio secundario benigna no reconocida (consulte la sección [8.2).](#82-implications-of-unrecognized-directory-entries)

<div id="table-36-vendor-extension-directoryentry" />

**Tabla 36 Vendor Extension DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#781-entrytype-field">la sección 7.8.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#782-generalsecondaryflags-field">la sección 7.8.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#783-vendorguid-field">la sección 7.8.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Este campo es obligatorio y los proveedores pueden definir su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1).](#641-entrytype-field)

##### <a name="7811-typecode-field"></a>7.8.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.1).](#6411-typecode-field)

Para la entrada del directorio Extensión de proveedor, el valor válido para este campo es 0.

##### <a name="7812-typeimportance-field"></a>7.8.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.2).](#6412-typeimportance-field)

Para la entrada del directorio Vendor Extension (Extensión de proveedor), el valor válido para este campo es 1.

##### <a name="7813-typecategory-field"></a>7.8.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.3).](#6413-typecategory-field)

##### <a name="7814-inuse-field"></a>Campo 7.8.1.4 InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.4).](#6414-inuse-field)

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 GeneralSecondaryFlags (Campo)

El campo GeneralSecondaryFlags se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2)](#642-generalsecondaryflags-field)y definirá el contenido del campo CustomDefined que se va a reservar.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 Campo AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2.1).](#6421-allocationpossible-field)

Para la entrada del directorio Extensión de proveedor, el valor válido para este campo es 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 Campo NoCompchain

El campo NoCompChain se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.2).](#6422-nofatchain-field)

#### <a name="783-vendorguid-field"></a>7.8.3 Campo VendorGuid

El campo VendorGuid debe contener un GUID que identifique de forma única la extensión de proveedor especificada.

Todos los valores posibles para este campo son válidos, excepto el GUID nulo, que es {00000000-0000-0000-0000-000000000000} . Sin embargo, los proveedores deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al definir sus extensiones.

El valor de este campo determina la estructura específica del proveedor del campo VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>7.9 Entrada del directorio de asignación de proveedores

La entrada del directorio Asignación de proveedor es una entrada de directorio secundario benigna en Conjuntos de entradas de directorio de archivos (consulte [la tabla 37).](#table-37-vendor-allocation-directoryentry) Un conjunto de entradas de directorio de archivo puede contener cualquier número de entradas de directorio de asignación de proveedor, hasta el límite de entradas de directorio secundario, menos el número de otras entradas de directorio secundario. Además, las entradas del directorio Asignación de proveedor solo son válidas si no preceden a las entradas de directorio extensión de secuencia y nombre de archivo necesarias.

Las entradas de directorio de asignación de proveedores permiten a los proveedores tener entradas de directorio únicas específicas del proveedor en conjuntos de entrada de directorio de archivos individuales a través del campo VendorGuid (consulte la tabla [37).](#table-37-vendor-allocation-directoryentry) Las entradas de directorio únicas permiten a los proveedores ampliar de forma eficaz el sistema de archivos ex LDAP. Los proveedores pueden definir el contenido de los clústeres asociados, si existen. Las implementaciones de proveedor pueden mantener el contenido de los clústeres asociados, si los hay, y pueden proporcionar funcionalidad específica del proveedor.

Las implementaciones que no reconocen el GUID de una entrada de directorio asignación de proveedor deben tratar la entrada de directorio igual que cualquier otra entrada de directorio secundario benigna no reconocida (consulte la sección [8.2).](#82-implications-of-unrecognized-directory-entries)

<div id="table-37-vendor-allocation-directoryentry" />

**Tabla 37 Vendor Allocation DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#791-entrytype-field">la sección 7.9.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y <a href="#792-generalsecondaryflags-field">la sección 7.9.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Este campo es obligatorio y <a href="#793-vendorguid-field">la sección 7.9.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Este campo es obligatorio y los proveedores pueden definir su contenido.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y <a href="#794-firstcluster-field">la sección 7.9.4</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y <a href="#795-datalength-field">la sección 7.9.5</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 Campo EntryType

El campo EntryType se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1).](#641-entrytype-field)

##### <a name="7911-typecode-field"></a>7.9.1.1 Campo TypeCode

El campo TypeCode se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.1).](#6411-typecode-field)

Para la entrada del directorio Asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7912-typeimportance-field"></a>7.9.1.2 Campo TypeImportance

El campo TypeImportance se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.2).](#6412-typeimportance-field)

Para la entrada del directorio Asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7913-typecategory-field"></a>7.9.1.3 Campo TypeCategory

El campo TypeCategory se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.3).](#6413-typecategory-field)

##### <a name="7914-inuse-field"></a>7.9.1.4 Campo InUse

El campo InUse se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.1.4).](#6414-inuse-field)

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 GeneralSecondaryFlags (Campo)

El campo GeneralSecondaryFlags se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte la sección [6.4.2)](#642-generalsecondaryflags-field)y definirá el contenido del campo CustomDefined que se va a reservar.

##### <a name="7921-allocationpossible-field"></a>7.9.2.1 Campo AllocationPossible

El campo AllocationPossible se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.1).](#6421-allocationpossible-field)

Para la entrada del directorio Asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7922-nofatchain-field"></a>7.9.2.2 Campo NoCompchain

El campo NoCompChain se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.2.2).](#6422-nofatchain-field)

#### <a name="793-vendorguid-field"></a>7.9.3 Campo VendorGuid

El campo VendorGuid debe contener un GUID que identifique de forma única la asignación de proveedor especificada.

Todos los valores posibles para este campo son válidos, excepto el GUID nulo, que es {00000000-0000-0000-0000-000000000000} . Sin embargo, los proveedores deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al definir sus extensiones.

El valor de este campo determina la estructura específica del proveedor del contenido de los clústeres asociados, si existe alguno.

#### <a name="794-firstcluster-field"></a>7.9.4 Campo FirstCluster

El campo FirstCluster se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.3).](#643-firstcluster-field)

#### <a name="795-datalength-field"></a>7.9.5 Campo DataLength

El campo DataLength se ajustará a la definición proporcionada en la plantilla Generic Secondary DirectoryEntry (consulte [la sección 6.4.4).](#644-datalength-field)

### <a name="710-texfat-padding-directory-entry"></a>7.10 Entrada de directorio de relleno de Texas LDAP

Esta especificación, ex LDAP Revision 1.00 File System Basic Specification( Especificación básica del sistema de archivos de la revisión 1.00), no define la entrada del directorio Padding de Texas LDAP. Sin embargo, su código de tipo es 1 y su importancia de tipo es 1. Las implementaciones de esta especificación deben tratar las entradas del directorio De relleno de Texas QUE no se reconocen igual que cualquier otra entrada de directorio principal benigna no reconocida; las implementaciones no moverán las entradas del directorio de relleno de LaRegistro de Texas QUE no se reconocen.

## <a name="8-implementation-notes"></a>8 Notas de implementación

### <a name="81-recommended-write-ordering"></a>8.1 Ordenación de escritura recomendada

Las implementaciones deben garantizar que el volumen sea lo más resistente posible a errores de alimentación y otros errores inevitables. Al crear nuevas entradas de directorio o modificar asignaciones de clúster, las implementaciones deben seguir este orden de escritura:

1. Establezca el valor del campo VolumeDirty en 1.

2. Actualice el FAT activo, si es necesario.

3. Actualización del mapa de bits de asignación activo

4. Cree o actualice la entrada del directorio, si es necesario.

5. Borre el valor del campo VolumeDirty en 0, si su valor anterior al primer paso era 0.

Al eliminar entradas de directorio o liberar asignaciones de clúster, las implementaciones deben seguir este orden de escritura:

1. Establezca el valor del campo VolumeDirty en 1.

2. Elimine o actualice la entrada del directorio, si es necesario.

3. Actualice el FAT activo, si es necesario.

4. Actualización del mapa de bits de asignación activo

5. Borre el valor del campo VolumeDirty en 0, si su valor anterior al primer paso era 0.

### <a name="82-implications-of-unrecognized-directory-entries"></a>8.2 Implicaciones de entradas de directorio no reconocidas

Las especificaciones futuras de exUNDA del mismo número de revisión principal, 1 y número de revisión secundaria mayor que 0, pueden definir nuevas entradas de directorio principal, secundaria crítica e secundaria benigna. Solo las especificaciones ex LDAP de un número de revisión principal mayor pueden definir nuevas entradas críticas del directorio principal. Las implementaciones de esta especificación, ex RAID Revision 1.00 File System Basic Specification, deben ser capaces de montar y acceder a cualquier volumen ex RAID del número de revisión principal 1 y cualquier número de revisión menor. Esto presenta escenarios en los que una implementación puede encontrar entradas de directorio que no reconoce. A continuación se describen las implicaciones de estos escenarios:

1. La presencia de entradas de directorio principal críticas no reconocidas en el directorio raíz hace que el volumen no sea válido. La presencia de cualquier entrada crítica del directorio principal, excepto las entradas de directorio de archivo, en cualquier directorio no raíz, hace que el directorio de hospedaje no sea válido.

2. Las implementaciones no deben modificar las entradas de directorio principal benignas no reconocidas ni sus asignaciones de clúster asociadas. Sin embargo, al eliminar un directorio y solo al eliminar un directorio, las implementaciones eliminarán las entradas de directorio principal benignas no reconocidas y liberarán todas las asignaciones de clúster asociadas, si las hubiera.

3. Las implementaciones no deben modificar entradas de directorio secundario críticas no reconocidas ni sus asignaciones de clúster asociadas. La presencia de una o varias entradas de directorio secundarias críticas no reconocidas en un conjunto de entradas de directorio hace que no se reconoce todo el conjunto de entradas del directorio. Al eliminar un conjunto de entradas de directorio que contiene una o varias entradas de directorio secundario críticas no reconocidas, las implementaciones liberarán todas las asignaciones de clúster, si las hubiera, asociadas a entradas de directorio secundario críticas no reconocidas.
   Además, si el conjunto de entradas de directorio describe un directorio, las implementaciones pueden:

   - Recorrer el directorio

   - Enumerar las entradas de directorio que contiene

   - Eliminación de entradas de directorios contenidos

   - Mover entradas de directorio independiente a otro directorio

   Sin embargo, las implementaciones no deben:

   - Modificar entradas de directorio independiente, excepto eliminar, como se indicó

   - Creación de nuevas entradas de directorio independiente

   - Abrir entradas de directorio independiente, excepto recorrer y enumerar, como se indicó.

4. Las implementaciones no deben modificar las entradas de directorio secundario benignas no reconocidas ni sus asignaciones de clúster asociadas.
   Las implementaciones deben omitir las entradas de directorio secundario benignas no reconocidas. Al eliminar un conjunto de entradas de directorio, las implementaciones liberarán todas las asignaciones de clúster, si las hubiera, asociadas a entradas de directorio secundario benignas no reconocidas.

## <a name="9-file-system-limits"></a>9 Límites del sistema de archivos

### <a name="91-sector-size-limits"></a>9.1 Límites de tamaño del sector

El campo BytesPerSectorShift define los límites de tamaño de sector inferior y superior (que se evalúa como límite **inferior: 512 bytes; límite superior: 4096 bytes).**

### <a name="92-cluster-size-limits"></a>9.2 Límites de tamaño de clúster

El campo SectorsPerClusterShift define los límites de tamaño de clúster inferior y superior (límite **inferior: 1 sector; límite superior: 25 -- sectores BytesPerSectorShift,** que se evalúa como 32 MB).

### <a name="93-cluster-heap-size-limits"></a>9.3 Límites de tamaño del montón de clúster

El montón de clúster debe contener al menos espacio suficiente para hospedar las siguientes estructuras básicas del sistema de archivos: el directorio raíz, todos los mapas de bits de asignación y la tabla de mayúsculas y minúsculas.

El límite inferior de tamaño del montón de clúster es una función del límite de tamaño inferior de cada una de las estructuras básicas del sistema de archivos que residen en el montón de clúster. Incluso dado el clúster más pequeño posible (512 bytes), cada una de las estructuras básicas del sistema de archivos no necesita más de un clúster. Por lo tanto, el límite inferior **es: 2 clústeres + NumberOfPlants**, que se evalúa como 3 o 4 clústeres, dependiendo del valor del campo NumberOfRacs.

El límite superior de tamaño del montón de clústeres es una función sencilla del número máximo posible de clústeres, que el campo ClusterCount define (límite **superior: 2 <sup>32</sup>- 11 clústeres).** Independientemente del tamaño del clúster, este montón de clústeres tiene espacio suficiente para hospedar al menos las estructuras básicas del sistema de archivos.

### <a name="94-volume-size-limits"></a>9.4 Límites de tamaño de volumen

El campo VolumeLength define los límites de tamaño de volumen inferior y superior (límite inferior: **<sup>2 sectores 20/2</sup><sup>BytesPerSectorShift,</sup>** que se evalúa como 1 MB; **límite superior: 2 <sup>64</sup>- 1** sectores , que, dado el mayor tamaño de sector posible, se evalúa como aproximadamente 64 KB). Sin embargo, esta especificación no recomienda más de<sup>2 24</sup>- 2 clústeres en el montón de clústeres (consulte la sección [3.1.9](#319-clustercount-field)). Por lo tanto, el límite superior recomendado de un volumen es: ClusterHeapOffset + (2<sup>24</sup>- 2) \* 2<sup>SectorsPerClusterShift</sup>. Dado el mayor tamaño de clúster posible, 32 MB, y suponiendo que ClusterHeapOffset sea de 96 MB (suficiente espacio para las regiones Main y Backup Boot y solo la primera FAT), el límite superior recomendado de un volumen se evalúa como aproximadamente de 512 TB.

### <a name="95-directory-size-limits"></a>9.5 Límites de tamaño de directorio

El campo DataLength de la entrada del directorio stream extension define los límites de tamaño de directorio inferior y superior (límite **inferior: 0 bytes; límite superior: 256 MB).** Esto significa que un directorio puede hospedar hasta 8 388 608 entradas de directorio (cada entrada de directorio consume 32 bytes). Dado el menor conjunto posible de entradas de directorio de archivos, tres entradas de directorio, un directorio puede hospedar hasta 2 796 202 archivos.

## <a name="10-appendix"></a>10 Apéndice

### <a name="101-globally-unique-identifiers-guids"></a>10.1 Identificadores únicos globales (GUID)

Un GUID es la implementación de Microsoft de un identificador único universal. Un GUID es un valor de 128 bits que consta de un grupo de 8 dígitos hexadecimales, seguido de tres grupos de 4 dígitos hexadecimales cada uno y seguido de un grupo de 12 dígitos hexadecimales, por ejemplo {6B29FC40-CA47-1067-B31D-00DD010662DA}, (vea la tabla [38).](#table-38-guid-structure)

<div id="table-38-guid-structure" />

**Estructura GUID de la tabla 38**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>(bytes)</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Datos1</td>
<td>0</td>
<td>4</td>
<td>Este campo es obligatorio y contiene los cuatro bytes del primer grupo del GUID (6B29FC40h del ejemplo).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y contiene los dos bytes del segundo grupo del GUID (CA47h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Este campo es obligatorio y contiene los dos bytes del tercer grupo del GUID (1067 h del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4[0]</td>
<td>8</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el byte más significativo del cuarto grupo del GUID (B3h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4[1]</td>
<td>9</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el byte menos significativo del cuarto grupo del GUID (1Dh del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4[2]</td>
<td>10</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el primer byte del quinto grupo del GUID (00 h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4[3]</td>
<td>11</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el segundo byte del quinto grupo del GUID (DDh del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4[4]</td>
<td>12</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el tercer byte del quinto grupo del GUID (01h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4[5]</td>
<td>13</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el cuarto byte del quinto grupo del GUID (06 h del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4[6]</td>
<td>14</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el quinto byte del quinto grupo del GUID (62 horas del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4[7]</td>
<td>15</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el sexto byte del quinto grupo del GUID (DAh del ejemplo).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10.2 Tablas de particiones

Para garantizar la interoperabilidad de los volúmenes ex RAID en un amplio conjunto de escenarios de uso, las implementaciones deben usar el tipo de partición 07h para el almacenamiento con particiones MBR y el GUID de partición {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} para el almacenamiento con particiones GPT.

## <a name="11-documentation-change-history"></a>11 Historial de cambios de documentación

En la tabla 39 se describe el historial de versiones de, correcciones, adiciones, eliminaciones de y aclaraciones de este documento.

<div id="table-39-documentation-change-history" />

**Historial de cambios de documentación de la tabla 39**

<table>
<thead>
<tr class="header">
<th><strong>Fecha</strong></th>
<th><strong>Descripción del cambio</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Jan-2008</td>
<td><p>Primera versión de la especificación básica, que incluye:</p>
<blockquote>
<p>Sección 1, Introducción</p>
<p>Sección 2,<br />
Estructura del volumen</p>
<p>Sección 3, Regiones de arranque principal y de copia de seguridad</p>
<p>Sección 4, Región de tabla de asignación de archivos</p>
<p>Sección 5, Región de datos</p>
<p>Sección 6, Estructura de directorios</p>
<p>Sección 7, Definiciones de entrada de directorio</p>
<p>Sección 8, Notas de implementación</p>
<p>Sección 9, Límites del sistema de archivos</p>
<p>Sección 10, Apéndice</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-Jun-2008</td>
<td><p>Segunda versión de la especificación básica, que incluye los siguientes cambios:</p>
<blockquote>
<p>Adición de la sección 11,<br />
Historial de cambios de documentación</p>
<p>Adición de las entradas del directorio Vendor Extension y Vendor Allocation en las secciones 7.8 y 7.9</p>
<p>Adición de la tabla de mayúsculas y minúsculas recomendada en las secciones 7.2.5 y 7.2.5.1</p>
<p>Adición de los campos UtcOffset en la sección 7.4 y adición del acrónimo UTC en la sección 1.3</p>
<p>Corrección del tamaño del campo CustomDefined en la tabla 19</p>
<p>Corrección del intervalo válido de valores NameLength en la sección 7.6.3</p>
<p>Corrección y aclaración de los campos Timestamp y 10msIncrement de la sección 7.4</p>
<p>Aclaración de la estructura de parámetros NULL en la sección 3.3</p>
<p>Aclaración del significado de los valores del campo NoCompChain de la sección 6.3.4.2</p>
<p>Aclaración del significado de los valores del campo DataLength en la sección 6.2.3</p>
<p>Aclaración del campo VolumeDirty de la sección 3.1.13.2 y ordenación de escritura recomendada en la sección 8.1</p>
<p>Aclaración del campo MediaFailure de la sección 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01 de octubre de 2008</td>
<td><p>Tercera versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Adición de SHALL, SHOULD y MAY a las explicaciones de campo</p>
<p>Adición de la definición utc en la sección 1.3 de la tabla 2</p>
<p>Se han modificado las secciones 1.5 para garantizar la alineación con el documento de especificación de TexasNTES.</p>
<p>Se ha aclarado la restricción de que solo Microsoft pueda definir el diseño de las entradas de directorio en la sección 6.2.</p>
<p>Se ha agregado una aclaración de que FirstCluster Field debe ser cero si DataLength es cero y NoReaChain está establecido en Section 6.3.5 y Section 6.4.3.</p>
<p>Se han aclarado los requisitos para las entradas válidas del directorio de archivos en la sección 7.4.</p>
<p>Se ha agregado el requisito de nombres de directorio y archivo únicos a la sección 7.7.</p>
<p>Se ha agregado la nota de implementación para ASCII al final de la sección 7.7.3.</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Cuarta versión de la especificación básica, que incluye los siguientes cambios:</p>
<blockquote>
<p>Se han quitado las referencias a Windows CE Access Control entradas</p>
<p>Se ha agregado una aclaración a la sección 7.2.5.1 para requerir explícitamente una tabla de casos completos</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-Sep-2009</td>
<td><p>Quinta versión de la especificación básica, que incluye los siguientes cambios:</p>
<blockquote>
<p>Cambios de formato de documento para permitir una mejor conversión de PDF</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24 de febrero de 2010</td>
<td><p>Sexta versión de la especificación básica, que incluye los siguientes cambios:</p>
<blockquote>
<p>Instrucción incorrecta modificada: "FirstCluster Field debe ser cero si el valor de DataLength es cero y no Se ha establecido NoApiChain" en la sección 6.3.5 y la sección 6.4.3 en "Si el bit NoApiChain es 1, FirstCluster debe apuntar a un clúster válido en el montón de clústeres" para aclarar que debe haber una asignación válida si se establece el bit NoRacChain.</p>
<p>Se ha agregado "Si el bit NoCompChain es 1, DataLength no debe ser cero. Si el campo FirstCluster es cero, DataLength también debe ser cero" en la sección 6.3.6 y la sección 6.4.4 para aclarar que debe haber una asignación válida si se establece el bit NoCompChain.</p>
<p>Aviso de copyright actualizado a 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26 de agosto de 2019</td>
<td><p>Sétima versión de la especificación básica, que incluye los siguientes cambios:</p>
<blockquote>
<p>Se han actualizado los términos legales relativos a la especificación, incluidos:</p>
<p>Eliminación del aviso confidencial de Microsoft</p>
<p>Eliminación de Microsoft Corporation de licencia de documentación técnica</p>
<p>Aviso de copyright actualizado a 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
