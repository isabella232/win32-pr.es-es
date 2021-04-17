---
description: Especificación del sistema de archivos exFat.
title: Especificación del sistema de archivos exFAT
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: c23a1f0c7aa9f0ad4752ce83cb734e753094c2cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720712"
---
# <a name="exfat-file-system-specification"></a>Especificación del sistema de archivos exFAT

## <a name="1-introduction"></a>1 Introducción

El sistema de archivos exFAT es el sucesor de FAT32 en la familia FAT de sistemas de archivos. Esta especificación describe el sistema de archivos exFAT y proporciona toda la información necesaria para implementar el sistema de archivos exFAT.

### <a name="11-design-goals"></a>1,1 objetivos de diseño

El sistema de archivos exFAT tiene tres objetivos de diseño central (vea la lista siguiente).

1. *Conserve la simplicidad de los sistemas de archivos basados en FAT.*

   > Dos de las ventajas de los sistemas de archivos basados en FAT son su simplicidad relativa y facilidad de implementación. En el espíritu de sus predecesores, los implementadores deberían encontrar exFAT relativamente sencillo y fácil de implementar.

2. *Habilitar archivos de gran tamaño y dispositivos de almacenamiento.*

   > El sistema de archivos exFAT usa 64 bits para describir el tamaño del archivo, lo que permite aplicaciones que dependen de archivos muy grandes. El sistema de archivos exFAT también permite clústeres tan grandes como 32 MB, habilitando eficazmente dispositivos de almacenamiento muy grandes.

3. *Incorpore la extensibilidad para futuras innovaciones.*

   > El sistema de archivos exFAT incorpora extensibilidad en su diseño, lo que permite que el sistema de archivos siga el ritmo de las innovaciones en el almacenamiento y los cambios de uso.

### <a name="12-specific-terminology"></a>1,2 terminología específica

En el contexto de esta especificación, ciertos términos (vea la [tabla 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) llevan un significado específico para el diseño y la implementación del sistema de archivos exFAT.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabla 1 definición de términos que llevan un significado muy específico**

<table>
<thead>
<tr class="header">
<th><strong>Término</strong></th>
<th><strong>Definición</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Deben</td>
<td>Esta especificación usa el término "debe" para describir un comportamiento que es obligatorio.</td>
</tr>
<tr class="even">
<td>Posible</td>
<td>Esta especificación usa el término "debe" para describir un comportamiento que recomienda encarecidamente, pero no hace obligatorio.</td>
</tr>
<tr class="odd">
<td>May</td>
<td>Esta especificación usa el término "puede" para describir un comportamiento que es opcional.</td>
</tr>
<tr class="even">
<td>Mandatory</td>
<td>Este término describe un campo o estructura que una implementación de debe modificar y debe interpretarse como se describe en esta especificación.</td>
</tr>
<tr class="odd">
<td>Opcionales</td>
<td>Este término describe un campo o estructura que una implementación puede admitir o no. Si una implementación de admite un campo o una estructura opcional determinados, debe modificar e interpretar el campo o la estructura como se describe en esta especificación.</td>
</tr>
<tr class="even">
<td>No definido</td>
<td>Este término describe el contenido del campo o de la estructura que una implementación puede modificar según sea necesario (es decir, desactive la opción cero al establecer los campos o estructuras circundantes) y no debe interpretarse para que contenga un significado específico.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td><p>Este término describe el contenido del campo o la estructura que implementa:</p>
<ol type="1">
<li><p>Se inicializará en cero y no debe usarse para ningún propósito</p></li>
<li><p>No debe interpretarse, excepto cuando se calculan sumas de comprobación</p></li>
<li><p>Conservará las operaciones que modifican campos o estructuras circundantes.</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1,3 texto completo de acrónimos comunes

Esta especificación usa acrónimos de uso común en el sector del equipo personal (consulte la [tabla 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabla 2 texto completo de acrónimos comunes**

| **Acrónimo** | **Texto completo**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Sistema básico de salida de entrada                          |
| CPU         | Unidad de procesamiento central                            |
| exFAT       | Tabla de asignación de archivos extensible                   |
| FAT         | Tabla de asignación de archivos                              |
| FAT12       | Tabla de asignación de archivos, índices de clúster de 12 bits      |
| FAT16       | Tabla de asignación de archivos, índices de clúster de 16 bits      |
| FAT32       | Tabla de asignación de archivos, índices de clúster de 32 bits      |
| GPT         | tabla de particiones GUID                               |
| GUID        | Identificador único global (consulte la [sección 10,1](#101-globally-unique-identifiers-guids))      |
| INT         | Interrupción                                          |
| MBR         | registro de arranque maestro                                 |
| texFAT      | ExFAT de transacciones seguras                             |
| UTC         | Hora universal coordinada                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1,4 calificadores de campo y estructura predeterminados

Los campos y las estructuras de esta especificación tienen los calificadores siguientes (vea la lista siguiente), a menos que la especificación tenga en cuenta lo contrario.

1. Sin signo

2. Usar notación decimal para describir valores, donde no se indica de otro modo; Esta especificación usa la letra "h" posterior a la corrección para denotar números hexadecimales y agrega GUID entre llaves

3. Están en formato Little-endian

4. No se requiere un carácter de terminación null para las cadenas

### <a name="15-windows-ce-and-texfat"></a>1,5 Windows CE y TexFAT

TexFAT es una extensión de exFAT que agrega la semántica operativa con seguridad de las transacciones en la parte superior del sistema de archivos base. Windows CE usa TexFAT.
TexFAT requiere el uso de las dos grasas y mapas de bits de asignación para su uso en transacciones. También define varias estructuras adicionales, entre las que se incluyen los descriptores de relleno y los descriptores de seguridad.

## <a name="2-volume-structure"></a>2 estructura de volumen

Un volumen es el conjunto de todas las estructuras del sistema de archivos y el espacio de datos necesario para almacenar y recuperar datos de usuario. Todos los volúmenes exFAT contienen cuatro regiones (vea la [tabla 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Tabla 3 estructura de volumen**

<table>
<thead>
<tr class="header">
<th><strong>Nombre de la subregión</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>organismos</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>sector</strong></p></th>
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
<td>Esta subregión es obligatoria y la <a href="#31-main-and-backup-boot-sector-sub-regions">sección 3,1</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Sectores principales de arranque extendidos</td>
<td>1</td>
<td>8</td>
<td>Esta subregión es obligatoria y la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">sección 3,2</a>) define su contenido.</td>
</tr>
<tr class="even">
<td>Parámetros principales del OEM</td>
<td>9</td>
<td>1</td>
<td>Esta subregión es obligatoria y la <a href="#33-main-and-backup-oem-parameters-sub-regions">sección 3,3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Principal reservado</td>
<td>10</td>
<td>1</td>
<td>Esta subregión es obligatoria y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>Suma de comprobación de arranque principal</td>
<td>11</td>
<td>1</td>
<td>Esta subregión es obligatoria y la <a href="#34-main-and-backup-boot-checksum-sub-regions">sección 3,4</a> define su contenido.</td>
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
<td>Esta subregión es obligatoria y la <a href="#31-main-and-backup-boot-sector-sub-regions">sección 3,1</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Copia de seguridad de sectores de arranque extendidos</td>
<td>13</td>
<td>8</td>
<td>Esta subregión es obligatoria y la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">sección 3,2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Parámetros de OEM de copia de seguridad</td>
<td>21</td>
<td>1</td>
<td>Esta subregión es obligatoria y la <a href="#33-main-and-backup-oem-parameters-sub-regions">sección 3,3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Copia de seguridad reservada</td>
<td>22</td>
<td>1</td>
<td>Esta subregión es obligatoria y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>Suma de comprobación de backup boot</td>
<td>23</td>
<td>1</td>
<td>Esta subregión es obligatoria y la <a href="#34-main-and-backup-boot-checksum-sub-regions">sección 3,4</a> define su contenido.</td>
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
<td><p>Esta subregión es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Primera FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Esta subregión es obligatoria y la <a href="#41-first-and-second-fat-sub-regions">sección 4,1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset y FatLength.</p></td>
</tr>
<tr class="even">
<td>Segunda FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1)</td>
<td><p>Esta subregión es obligatoria y la <a href="#41-first-and-second-fat-sub-regions">sección 4,1</a> define su contenido, si existe.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset, FatLength y NumberOfFats. El campo NumberOfFats solo puede contener los valores 1 y 2.</p></td>
</tr>
<tr class="odd">
<td><strong>Región de datos</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Alineación del montón del clúster</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset – (FatOffset + FatLength * NumberOfFats)</td>
<td><p>Esta subregión es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos FatOffset, FatLength, NumberOfFats y ClusterHeapOffset. Los valores válidos del campo NumberOfFats son 1 y 2.</p></td>
</tr>
<tr class="odd">
<td>Montón de clústeres</td>
<td>ClusterHeapOffset</td>
<td>Clustercount, * 2<sup>SectorsPerClusterShift</sup></td>
<td><p>Esta subregión es obligatoria y la <a href="#51-cluster-heap-sub-region">sección 5,1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset, Clustercount, y SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Exceso de espacio</td>
<td>ClusterHeapOffset + Clustercount, * 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + Clustercount, * 2<sup>SectorsPerClusterShift</sup>)</td>
<td><p>Esta subregión es obligatoria y su contenido, si existe, no está definido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset, Clustercount,, SectorsPerClusterShift y VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 regiones de arranque principales y de copia de seguridad

La región de arranque principal proporciona todas las instrucciones necesarias para el arranque, información de identificación y parámetros del sistema de archivos para permitir que una implementación realice lo siguiente:

1. Arranque: Sujete un equipo desde un volumen exFAT.

2. Identifique el sistema de archivos en el volumen como exFAT.

3. Detecta la ubicación de las estructuras del sistema de archivos exFAT.

La región de arranque de copia de seguridad es una copia de seguridad de la región de arranque principal. Ayuda a recuperar el volumen exFAT en caso de que la región de arranque principal esté en un estado incoherente. Excepto en circunstancias poco frecuentes, como la actualización de instrucciones para el arranque, las implementaciones no deben modificar el contenido de la región de arranque de copia de seguridad.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3,1 subregiones del sector de arranque principal y de copia de seguridad

El sector de arranque principal contiene código para el arranque desde un volumen de exFAT y parámetros básicos de exFAT que describen la estructura del volumen (vea la [tabla 4](#table-4-main-and-backup-boot-sector-structure)). BIOS, MBR u otros agentes de programa previo de arranque pueden inspeccionar este sector y cargar y ejecutar las instrucciones de arranque que contiene.

El sector de arranque de copia de seguridad es una copia de seguridad del sector de arranque principal y tiene la misma estructura (vea la [tabla 4](#table-4-main-and-backup-boot-sector-structure)). El sector de arranque de copia de seguridad puede ayudar a las operaciones de recuperación. sin embargo, las implementaciones de deben tratar el contenido de los campos VolumeFlags y PercentInUse como obsoletos.

Antes de usar el contenido del sector de arranque principal o de copia de seguridad, las implementaciones comprobarán su contenido mediante la validación de la suma de comprobación de arranque correspondiente y la garantía de que todos los campos estén dentro de su intervalo de valores válido.

Mientras que la operación de formato inicial inicializará el contenido de los sectores principal y de arranque de copia de seguridad, las implementaciones pueden actualizar estos sectores (y también actualizarán su correspondiente suma de comprobación de arranque) según sea necesario. Sin embargo, las implementaciones pueden actualizar los campos VolumeFlags o PercentInUse sin actualizar su correspondiente suma de comprobación de arranque (la suma de comprobación excluye específicamente estos dos campos).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabla 4 estructura del sector de arranque principal y de copia de seguridad**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Este campo es obligatorio y la <a href="#311-jumpboot-field">sección 3.1.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#312-filesystemname-field">sección 3.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Este campo es obligatorio y la <a href="#313-mustbezero-field">sección 3.1.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#314-partitionoffset-field">sección 3.1.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#315-volumelength-field">sección 3.1.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#316-fatoffset-field">sección 3.1.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#317-fatlength-field">sección 3.1.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#318-clusterheapoffset-field">sección 3.1.8</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Clustercount,</td>
<td>92</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#319-clustercount-field">sección 3.1.9</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3110-firstclusterofrootdirectory-field">sección 3.1.10</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3111-volumeserialnumber-field">sección 3.1.11</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#3112-filesystemrevision-field">sección 3.1.12</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#3113-volumeflags-field">sección 3.1.13</a> define su contenido.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#3114-bytespersectorshift-field">sección 3.1.14</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#3115-sectorsperclustershift-field">sección 3.1.15</a> define su contenido.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#3116-numberoffats-field">sección 3.1.16</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#3117-driveselect-field">sección 3.1.17</a> define su contenido.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#3118-percentinuse-field">sección 3.1.18</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>113</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
<tr class="even">
<td>Arranque</td>
<td>120</td>
<td>390</td>
<td>Este campo es obligatorio y la <a href="#3119-bootcode-field">sección 3.1.19</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#3120-bootsignature-field">sección 3.1.20</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> : 512</td>
<td><p>Este campo es obligatorio y su contenido, si existe, no está definido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot campo

El campo JumpBoot contendrá la instrucción de salto para las CPU comunes en los equipos personales, que, cuando se ejecuten, "saltan" la CPU para ejecutar las instrucciones de arranque en el campo de arranque.

El valor válido para este campo es (en orden de byte de orden inferior a byte de orden superior) EBh 76h 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 campo FileSystemName

El campo FileSystemName debe contener el nombre del sistema de archivos del volumen.

El valor válido para este campo es, en caracteres ASCII, "EXFAT", que incluye tres espacios en blanco al final.

#### <a name="313-mustbezero-field"></a>3.1.3 campo MustBeZero

El campo MustBeZero se corresponderá directamente con el intervalo de bytes que consume el bloque de parámetros BIOS empaquetados en los volúmenes FAT12/16/32.

El valor válido para este campo es 0, lo que ayuda a evitar que las implementaciones de FAT12/16/32 monten por error un volumen exFAT.

#### <a name="314-partitionoffset-field"></a>3.1.4 campo PartitionOffset

El campo PartitionOffset debe describir el desplazamiento del sector relativo al medio de la partición que hospeda el volumen exFAT determinado. Este campo ayuda con el arranque desde el volumen mediante el uso extendido de INT 13h en equipos personales.

Todos los valores posibles para este campo son válidos; sin embargo, el valor 0 indica que las implementaciones deben omitir este campo.

#### <a name="315-volumelength-field"></a>3.1.5 VolumeLength

El campo VolumeLength debe describir el tamaño del volumen de exFAT determinado en sectores.

El intervalo válido de valores para este campo debe ser:

- Al menos 2<sup>20</sup>/2<sup>BytesPerSectorShift</sup>, lo que garantiza que el volumen más pequeño no sea inferior a 1 MB.

- Como máximo 2<sup>64</sup>-1, el valor más grande que puede describir este campo

Sin embargo, si el tamaño de la subregión de espacio sobrante es 0, el valor de este campo es ClusterHeapOffset + (2<sup>32</sup>-11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 FatOffset

El campo FatOffset debe describir el desplazamiento de sector relativo al volumen de la primera FAT. Este campo permite que las implementaciones alineen la primera FAT con las características de los medios de almacenamiento subyacentes.

El intervalo válido de valores para este campo debe ser:

- Al menos 24, que tiene en cuenta los sectores que consumen las regiones de arranque principales y de copia de seguridad

- A lo sumo ClusterHeapOffset-(FatLength \* NumberOfFats), que tiene en cuenta los sectores que consume el montón de clústeres

#### <a name="317-fatlength-field"></a>3.1.7 FatLength

El campo FatLength debe describir la longitud, en sectores, de cada tabla FAT (el volumen puede contener hasta dos grasas).

El intervalo válido de valores para este campo debe ser:

- Al menos (Clustercount, + 2) \* 2<sup>2</sup>/2<sup>BytesPerSectorShift</sup>redondeado al entero más próximo, lo que garantiza que cada FAT tenga espacio suficiente para describir todos los clústeres del montón del clúster

- Como máximo (ClusterHeapOffset-FatOffset)/NumberOfFats redondeado al entero más próximo, lo que garantiza que las grasas existen antes que el montón del clúster.

Este campo puede contener un valor que supere el límite inferior (como se describió anteriormente) para permitir que la segunda FAT, si está presente, se alinee también con las características de los medios de almacenamiento subyacentes. El contenido del espacio que supera lo que el propio elemento FAT requiere, si existe, no está definido.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 ClusterHeapOffset

El campo ClusterHeapOffset debe describir el desplazamiento de sector relativo al volumen del montón del clúster. Este campo permite que las implementaciones alineen el montón del clúster con las características de los medios de almacenamiento subyacentes.

El intervalo válido de valores para este campo debe ser:

- Al menos FatOffset + FatLength \* NumberOfFats, para tener en cuenta los sectores que consumen todas las regiones anteriores

- Como máximo 2<sup>32</sup>-1 o VolumeLength-(Clustercount, \* 2<sup>SectorsPerClusterShift</sup>), lo que sea menor

#### <a name="319-clustercount-field"></a>3.1.9 Clustercount,

El campo Clustercount, debe describir el número de clústeres que contiene el montón de clústeres.

El valor válido para este campo debe ser el menor de los siguientes:

- (VolumeLength-ClusterHeapOffset)/2<sup>SectorsPerClusterShift</sup>redondeado al entero más cercano, que es exactamente el número de clústeres que pueden caber entre el principio del montón del clúster y el final del volumen.

- 2<sup>32</sup>-11, que es el número máximo de clústeres que puede describir una FAT

El valor del campo Clustercount, determina el tamaño mínimo de una FAT. Para evitar las grasas muy grandes, las implementaciones pueden controlar el número de clústeres en el montón del clúster aumentando el tamaño del clúster (a través del campo SectorsPerClusterShift). Esta especificación recomienda no tener más de<sup>dos</sup>clústeres en el montón de clústeres. Sin embargo, las implementaciones deben ser capaces de controlar volúmenes con hasta 2 clústeres<sup>32</sup>-11 en el montón del clúster.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 FirstClusterOfRootDirectory

El campo FirstClusterOfRootDirectory debe contener el índice de clúster del primer clúster del directorio raíz. Las implementaciones deben hacer todo lo posible para colocar el primer clúster del directorio raíz en el primer clúster no incorrecto después de que los clústeres consuman el mapa de bits de asignación y la tabla de casos de uso.

El intervalo válido de valores para este campo debe ser:

- Al menos 2, el índice del primer clúster en el montón del clúster

- Como máximo Clustercount, + 1, el índice del último clúster en el montón del clúster

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 VolumeSerialNumber

El campo VolumeSerialNumber debe contener un número de serie único. Esto ayuda a las implementaciones a distinguir entre distintos volúmenes de exFAT.
Las implementaciones deben generar el número de serie combinando la fecha y hora de formato del volumen exFAT. El mecanismo de combinación de fecha y hora para formar un número de serie es específico de la implementación.

Todos los valores posibles para este campo son válidos.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 FileSystemRevision

El campo FileSystemRevision debe describir los números de revisión principales y secundarios de las estructuras exFAT en el volumen especificado.

El byte de orden superior es el número de revisión principal y el byte de orden inferior es el número de revisión secundaria. Por ejemplo, si el byte de orden superior contiene el valor 01h y si el byte de orden inferior contiene el valor 05h, el campo FileSystemRevision describe el número de revisión 1,05.
Del mismo modo, si el byte de orden superior contiene el valor 0Ah y si el byte de orden inferior contiene el valor 0Fh, el campo FileSystemRevision describe el número de revisión 10,15.

El intervalo válido de valores para este campo debe ser:

- Al menos 0 para el byte de orden inferior y 1 para el byte de orden superior

- Como máximo 99 para el byte de orden inferior y 99 para el byte de orden superior

El número de revisión de exFAT que describe esta especificación es 1,00.
Las implementaciones de esta especificación deben montar cualquier volumen de exFAT con la revisión principal número 1 y no debe montar ningún volumen exFAT con cualquier otro número de revisión principal. Las implementaciones respetarán el número de revisión menor y no realizarán operaciones ni creará ninguna estructura del sistema de archivos que no se haya descrito en la especificación correspondiente del número de revisión secundaria.

#### <a name="3113-volumeflags-field"></a>3.1.13 VolumeFlags

El campo VolumeFlags contendrá marcas que indican el estado de varias estructuras del sistema de archivos en el volumen exFAT (vea la [tabla 5](#table-5-volumeflags-field-structure)).

Las implementaciones no incluirán este campo al calcular la suma de comprobación de la región de arranque de copia de seguridad o arranque principal correspondiente. Cuando se hace referencia al sector de arranque de la copia de seguridad, las implementaciones tratarán este campo como obsoleto.

<div id="table-5-volumeflags-field-structure" />

**Tabla 5 VolumeFlags estructura de campo**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#31131-activefat-field">sección 3.1.13.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#31132-volumedirty-field">sección 3.1.13.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#31133-mediafailure-field">sección 3.1.13.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#31134-cleartozero-field">sección 3.1.13.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>4</td>
<td>12</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 ActiveFat

El campo ActiveFat debe describir qué mapa de bits de asignación y FAT están activos (y las implementaciones deben usar), como se indica a continuación:

- 0, que significa que el primer mapa de bits de la primera asignación y FAT están activos

- 1, lo que significa que el segundo mapa de bits de asignación de FAT y segundo están activos y solo es posible cuando el campo NumberOfFats contiene el valor 2

Las implementaciones considerarán la FAT inactiva y el mapa de bits de asignación como obsoletos. Solo las implementaciones compatibles con TexFAT conmutarán los mapas de bits activos de FAT y de asignación (consulte la [sección 7,1](#71-allocation-bitmap-directory-entry)).

##### <a name="31132-volumedirty-field"></a>3.1.13.2 VolumeDirty

El campo VolumeDirty debe describir si el volumen está sucio o no, como se indica a continuación:

- 0, que significa que el volumen probablemente está en un estado coherente

- 1, lo que significa que el volumen probablemente esté en un estado incoherente

Las implementaciones deben establecer el valor de este campo en 1 al encontrar incoherencias en los metadatos del sistema de archivos que no se resuelven. Si, al montar un volumen, el valor de este campo es 1, solo las implementaciones que resuelvan incoherencias en los metadatos del sistema de archivos pueden borrar el valor de este campo a 0. Estas implementaciones solo borrarán el valor de este campo a 0 después de asegurarse de que el sistema de archivos se encuentra en un estado coherente.

Si, al montar un volumen, el valor de este campo es 0, las implementaciones deben establecer este campo en 1 antes de actualizar los metadatos del sistema de archivos y borrar este campo a 0 después, de forma similar al orden de escritura recomendado descrito en la [sección 8,1](#81-recommended-write-ordering).

##### <a name="31133-mediafailure-field"></a>3.1.13.3 MediaFailure

El campo MediaFailure debe describir si una implementación ha detectado errores de medios o no, como se indica a continuación:

- 0, que significa que el medio de hospedaje no ha comunicado errores o que los errores conocidos ya se han registrado en la FAT como clústeres "incorrectos"

- 1, lo que significa que el medio de hospedaje ha detectado errores (es decir, que se ha producido un error en las operaciones de lectura o escritura)

Una implementación debe establecer este campo en 1 cuando:

1. El medio de hospedaje produce un error en los intentos de acceso a cualquier región del volumen

2. La implementación ha agotado los algoritmos de reintento de acceso, si los hay.

Si, al montar un volumen, el valor de este campo es 1, las implementaciones que examinan todo el volumen en busca de errores de medios y registran todos los errores como clústeres "incorrectos" en la FAT (o que resuelven los errores de los medios) pueden borrar el valor de este campo a 0.

##### <a name="31134-cleartozero-field"></a>3.1.13.4 ClearToZero

El campo ClearToZero no tiene un significado significativo en esta especificación.

Los valores válidos para este campo son:

- 0, que no tiene ningún significado determinado

- 1, lo que significa que las implementaciones deben desactivar este campo en 0 antes de modificar cualquier estructura, directorio o archivo del sistema de archivos

#### <a name="3114-bytespersectorshift-field"></a>3.1.14 BytesPerSectorShift

El campo BytesPerSectorShift debe describir los bytes por sector expresado como registro<sub>2</sub>(n), donde N es el número de bytes por sector. Por ejemplo, para 512 bytes por sector, el valor de este campo es 9.

El intervalo válido de valores para este campo debe ser:

- Al menos 9 (tamaño de sector de 512 bytes), que es el sector más pequeño posible para un volumen de exFAT

- Como máximo 12 (tamaño de sector de 4096 bytes), que es el tamaño de página de memoria de las CPU comunes en los equipos personales

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 SectorsPerClusterShift

El campo SectorsPerClusterShift debe describir los sectores por clúster expresados como registro<sub>2</sub>(n), donde N es el número de sectores por clúster. Por ejemplo, para 8 sectores por clúster, el valor de este campo es 3.

El intervalo válido de valores para este campo debe ser:

- Al menos 0 (1 sector por clúster), que es el clúster más pequeño posible

- Como máximo 25-BytesPerSectorShift, que se evalúa como un tamaño de clúster de 32 MB

#### <a name="3116-numberoffats-field"></a>3.1.16 NumberOfFats

El campo NumberOfFats debe describir el número de grasas y los mapas de bits de asignación que contiene el volumen.

El intervalo válido de valores para este campo debe ser:

- 1, que indica que el volumen solo contiene el primer mapa de bits de la primera distribución y FAT

- 2, que indica que el volumen contiene el primer mapa de bits FAT, segunda FAT, primera asignación y segundo mapa de bits de asignación; Este valor solo es válido para los volúmenes TexFAT

#### <a name="3117-driveselect-field"></a>3.1.17 DriveSelect

El campo DriveSelect debe contener el número de unidad INT 13h extendido, que ayuda a partir de este volumen mediante el uso del INT.

Todos los valores posibles para este campo son válidos. Los campos similares en sistemas de archivos basados en FAT anteriores contenían con frecuencia el valor 80h.

#### <a name="3118-percentinuse-field"></a>3.1.18 PercentInUse

El campo PercentInUse debe describir el porcentaje de clústeres en el montón de clúster que se asignan.

El intervalo válido de valores para este campo debe ser:

- Entre 0 y 100, ambos inclusive, que es el porcentaje de clústeres asignados en el montón del clúster, redondeado al entero más cercano

- Exactamente FFh, que indica que el porcentaje de clústeres asignados en el montón del clúster no está disponible

Las implementaciones deben cambiar el valor de este campo para reflejar los cambios en la asignación de clústeres en el montón del clúster o cambiarlos a FFh.

Las implementaciones no incluirán este campo al calcular la suma de comprobación de la región de arranque de copia de seguridad o arranque principal correspondiente. Cuando se hace referencia al sector de arranque de la copia de seguridad, las implementaciones tratarán este campo como obsoleto.

#### <a name="3119-bootcode-field"></a>3.1.19 campo de arranque

El campo de arranque debe contener instrucciones de arranque.
Las implementaciones pueden rellenar este campo con las instrucciones de CPU necesarias para el arranque de un sistema informático. Las implementaciones que no proporcionan instrucciones para el arranque inicializarán cada byte de este campo en F4h (la instrucción Halt para las CPU comunes en los equipos personales) como parte de la operación de formato.

#### <a name="3120-bootsignature-field"></a>3.1.20 BootSignature

El campo BootSignature debe describir si el propósito de un sector determinado es que sea un sector de arranque o no.

El valor válido para este campo es AA55h. Cualquier otro valor de este campo invalida su sector de arranque respectivo. Las implementaciones deben comprobar el contenido de este campo antes de depender de cualquier otro campo en el sector de arranque respectivo.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3,2 subregiones de sectores de arranque principales y de copia de seguridad

Cada sector de los sectores de arranque extendidos principales tiene la misma estructura. sin embargo, cada sector puede contener instrucciones diferentes para el arranque (vea la tabla 6). Los agentes de arranque previo, como las instrucciones para el arranque en el sector de arranque principal, las implementaciones de BIOS alternativas o el firmware de un sistema incrustado, pueden cargar estos sectores y ejecutar las instrucciones que contienen.

Los sectores de arranque extendido de copia de seguridad son una copia de seguridad de los sectores de arranque extendidos principales y tienen la misma estructura (vea la [tabla 6](#table-6-extended-boot-sector-structure)).

Antes de ejecutar las instrucciones de los sectores de arranque principal o de copia de seguridad extendido, las implementaciones deben comprobar su contenido asegurándose de que el campo ExtendedBootSignature de cada sector contiene su valor establecido.

Mientras que la operación de formato inicial inicializará el contenido de los sectores de arranque principal y de copia de seguridad extendido, las implementaciones pueden actualizar estos sectores (y también actualizarán su correspondiente suma de comprobación de arranque) según sea necesario.

<div id="table-6-extended-boot-sector-structure" />

**Tabla 6 estructura del sector de arranque extendido**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> : 4</td>
<td><p>Este campo es obligatorio y la <a href="#321-extendedbootcode-field">sección 3.2.1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> : 4</td>
<td>4</td>
<td><p>Este campo es obligatorio y la <a href="#322-extendedbootsignature-field">sección 3.2.2</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 campo ExtendedBootCode

El campo ExtendedBootCode contendrá instrucciones para el arranque.
Las implementaciones pueden rellenar este campo con las instrucciones de CPU necesarias para el arranque de un sistema informático. Las implementaciones que no proporcionan instrucciones para el arranque inicializarán cada byte de este campo a 00H como parte de la operación de formato.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 campo ExtendedBootSignature

El campo ExtendedBootSignature debe describir si el objetivo del sector determinado es que sea un sector de arranque extendido o no.

El valor válido para este campo es AA550000h. Cualquier otro valor de este campo invalida sus respectivos sectores de arranque principal o de copia de seguridad extendidos.
Las implementaciones deben comprobar el contenido de este campo antes de depender de cualquier otro campo en el sector de arranque extendido correspondiente.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>subregiones 3,3 principales y de copia de seguridad de parámetros OEM

La subregión principal de parámetros de OEM contiene diez estructuras de parámetros que pueden contener información específica del fabricante (vea la [Tabla 7](#table-7-oem-parameters-structure)). Cada una de las diez estructuras de parámetros deriva de la plantilla de parámetros genéricos (consulte la [sección 3.3.2](#332-generic-parameters-template)). Los fabricantes pueden derivar sus propias estructuras de parámetros personalizados de la plantilla de parámetros genéricos. Esta especificación define dos estructuras de parámetros: parámetros null (vea la [sección 3.3.3](#333-null-parameters)) y parámetros de Flash (consulte la [sección 3.3.4](#334-flash-parameters)).

Los parámetros de OEM de copia de seguridad son una copia de seguridad de los parámetros principales del OEM y tienen la misma estructura (vea la [Tabla 7](#table-7-oem-parameters-structure)).

Antes de usar el contenido de los parámetros principal o de copia de seguridad de OEM, las implementaciones comprobarán su contenido mediante la validación de la suma de comprobación de arranque correspondiente.

Los fabricantes deben rellenar los parámetros principales y de copia de seguridad de OEM con sus propias estructuras de parámetros personalizados, si las hay, y cualquier otra estructura de parámetros. Las operaciones de formato posteriores conservarán el contenido de los parámetros principales y de copia de seguridad de OEM.

Las implementaciones pueden actualizar los parámetros principales y de copia de seguridad de OEM según sea necesario (y también actualizarán su correspondiente suma de comprobación de arranque).

<div id="table-7-oem-parameters-structure" />

**Tabla 7 estructura de parámetros OEM**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parámetros [0]</td>
<td>0</td>
<td>48</td>
<td>Este campo es obligatorio y la <a href="#331-parameters0--parameters9">sección 3.3.1</a> define su contenido.</td>
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
<td>Parámetros [9]</td>
<td>432</td>
<td>48</td>
<td>Este campo es obligatorio y la <a href="#331-parameters0--parameters9">sección 3.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> : 480</td>
<td><p>Este campo es obligatorio y su contenido está reservado.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 parámetros \[ 0 \] ... Parámetros \[ 9\]

Cada campo de parámetros de esta matriz contiene una estructura de parámetros, que se deriva de la plantilla de parámetros genéricos (consulte la [sección 3.3.2](#332-generic-parameters-template)).
Cualquier campo de parámetros no usados se describe como si contiene una estructura de parámetros null (vea la [sección 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>3.3.2 plantilla de parámetros genéricos

La plantilla de parámetros genéricos proporciona la definición base de una estructura de parámetros (vea la [Tabla 8](#table-8-generic-parameters-template)). Todas las estructuras de parámetros derivan de esta plantilla. La compatibilidad con esta plantilla de parámetros genéricos es obligatoria.

<div id="table-8-generic-parameters-template" />

**Plantilla de parámetros genéricos de tabla 8**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#3321-parametersguid-field">sección 3.3.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla definen su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 ParametersGuid

El campo ParametersGuid debe describir un GUID, que determina el diseño del resto de la estructura de parámetros especificada.

Todos los valores posibles para este campo son válidos; sin embargo, los fabricantes deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al derivar estructuras de parámetros personalizados a partir de esta plantilla.

#### <a name="333-null-parameters"></a>3.3.3 parámetros null

La estructura de parámetros NULL se deriva de la plantilla de parámetros genéricos (consulte la [sección 3.3.2](#332-generic-parameters-template)) y describe un campo de parámetros no usados (vea la [Tabla 9](#table-9-null-parameters-structure)). Al crear o actualizar la estructura de parámetros OEM, las implementaciones deben rellenar los campos de parámetros no usados con la estructura de parámetros null. Además, al crear o actualizar la estructura de parámetros OEM, las implementaciones deben consolidar las estructuras de parámetros null al final de la matriz, con lo que se dejan todas las demás estructuras de parámetros al principio de la estructura de parámetros OEM.

La compatibilidad con la estructura de parámetros NULL es obligatoria.

<div id="table-9-null-parameters-structure" />

**Tabla 9 parámetros null (estructura)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#3331-parametersguid-field">sección 3.3.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>16</td>
<td>32</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 ParametersGuid

El campo ParametersGuid debe ajustarse a la definición proporcionada por la plantilla de parámetros genéricos (consulte la [sección 3.3.2.1](#3321-parametersguid-field)).

El valor válido para este campo, en notación GUID, es {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>3.3.4 parámetros de Flash

La estructura de parámetros de Flash deriva de la plantilla de parámetros genéricos (consulte la [sección 3.3.2](#332-generic-parameters-template)) y contiene los parámetros de los medios Flash (vea la [tabla 10](#table-10-flash-parameters-structure)). Los fabricantes de dispositivos de almacenamiento basados en Flash pueden rellenar un campo de parámetros (preferiblemente el campo de parámetros \[ 0 \] ) con esta estructura de parámetros. Las implementaciones pueden usar la información de la estructura de parámetros de Flash para optimizar las operaciones de acceso durante las lecturas y escrituras, y para la alineación de las estructuras del sistema de archivos Durning el formato del medio.

La compatibilidad con la estructura de parámetros de Flash es opcional.

<div id="table-10-flash-parameters-structure" />

**Tabla 10 parámetros de Flash (estructura)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#3341-parametersguid-field">sección 3.3.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3342-eraseblocksize-field">sección 3.3.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3343-pagesize-field">sección 3.3.4.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3344-sparesectors-field">sección 3.3.4.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3345-randomaccesstime-field">sección 3.3.4.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3346-programmingtime-field">sección 3.3.4.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3347-readcycle-field">sección 3.3.4.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#3348-writecycle-field">sección 3.3.4.8</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Reservado</td>
<td>44</td>
<td>4</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

Todos los valores posibles para todos los campos de parámetros de Flash, excepto para el campo ParametersGuid, son válidos. Sin embargo, el valor 0 indica que el campo no tiene sentido (las implementaciones omitirán el campo especificado).

##### <a name="3341-parametersguid-field"></a>3.3.4.1 ParametersGuid

El campo ParametersGuid debe ajustarse a la definición proporcionada en la plantilla de parámetros genéricos (consulte la [sección 3.3.2.1](#3321-parametersguid-field)).

El valor válido para este campo, en la notación GUID, es {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 EraseBlockSize

El campo EraseBlockSize debe describir el tamaño, en bytes, del bloque de borrado del medio Flash.

##### <a name="3343-pagesize-field"></a>3.3.4.3 campo de paginación

El campo PageSize debe describir el tamaño, en bytes de la página del medio Flash.

##### <a name="3344-sparesectors-field"></a>3.3.4.4 SpareSectors

El campo SpareSectors debe describir el número de sectores que el medio Flash tiene disponible para las operaciones de reserva internas.

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 RandomAccessTime

El campo RandomAccessTime debe describir el tiempo promedio de acceso aleatorio del medio Flash, en nanosegundos.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 ProgrammingTime

En el campo ProgrammingTime se describe el tiempo medio de programación del medio Flash, en nanosegundos.

##### <a name="3347-readcycle-field"></a>3.3.4.7 ReadCycle

El campo ReadCycle debe describir el tiempo promedio de ciclo de lectura del medio Flash, en nanosegundos.

##### <a name="3348-writecycle-field"></a>3.3.4.8 WriteCycle

El campo WriteCycle debe describir el tiempo medio del ciclo de escritura, en nanosegundos.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3,4 subregiones de suma de comprobación de arranque principal y de copia de seguridad

Las sumas de comprobación principal y de arranque de copia de seguridad contienen un patrón de repetición de la suma de comprobación de cuatro bytes del contenido de todas las demás subregiones en sus regiones de arranque respectivas. El cálculo de la suma de comprobación no incluirá los campos VolumeFlags y PercentInUse en el sector de arranque correspondiente (vea la [figura 1](#figure-1-boot-checksum-computation)). El patrón de repetición de la suma de comprobación de cuatro bytes rellena la subregión de la suma de comprobación de arranque correspondiente desde el principio hasta el final de la subregión.

Antes de usar el contenido de cualquiera de las demás subregiones en las regiones de arranque principal o de copia de seguridad, las implementaciones comprobarán su contenido mediante la validación de la suma de comprobación de arranque correspondiente.

Mientras que la operación de formato inicial rellenará las sumas de comprobación principal y de copia de seguridad con el patrón de suma de comprobación repetido, las implementaciones actualizarán estos sectores a medida que cambie el contenido de los demás sectores en sus respectivas regiones de arranque.

<div id="figure-1-boot-checksum-computation" />

**Figura 1 cálculo de la suma de comprobación de arranque**

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

## <a name="4-file-allocation-table-region"></a>4 región de tabla de asignación de archivos

La región de tabla de asignación de archivos (FAT) puede contener hasta dos grasas, una en la primera subregión de FAT y otra en la subregión de FAT.
El campo NumberOfFats describe cuántas grasas contiene esta región. Los valores válidos para el campo NumberOfFats son 1 y 2. Por lo tanto, la primera subregión de FAT siempre contiene una FAT. Si el campo NumberOfFats es dos, la segunda subregión FAT también contiene una FAT.

El campo ActiveFat del campo VolumeFlags describe qué FAT está activa. Solo el campo VolumeFlags del sector de arranque principal es actual.
Las implementaciones de deben tratar la FAT que no está activa como obsoleta. El uso de la FAT inactiva y el cambio entre grasas es específico de la implementación.

### <a name="41-first-and-second-fat-sub-regions"></a>subregiones 4,1 primera y segunda FAT

Una FAT debe describir las cadenas de clúster en el montón del clúster (vea la [tabla 11](#table-11-file-allocation-table-structure)).
Una cadena de clústeres es una serie de clústeres que proporciona espacio para grabar el contenido de archivos, directorios y otras estructuras del sistema de archivos. Una FAT representa una cadena de clúster como una lista vinculada individualmente de índices de clúster. Con la excepción de las dos primeras entradas, cada entrada de una FAT representa exactamente un clúster.

<div id="table-11-file-allocation-table-structure" />

**Tabla 11 estructura de la tabla de asignación de archivos**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry [0]</td>
<td>0</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#412-fatentry1-field">sección 4.1.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FatEntry [1]</td>
<td>4</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#412-fatentry1-field">sección 4.1.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FatEntry [2]</td>
<td>8</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#413-fatentry2--fatentryclustercount1-fields">sección 4.1.3</a> define su contenido.</td>
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
<td>FatEntry [Clustercount, + 1]</td>
<td>(Clustercount, + 1) * 4</td>
<td>4</td>
<td><p>Este campo es obligatorio y la <a href="#413-fatentry2--fatentryclustercount1-fields">sección 4.1.3</a> define su contenido.</p>
<p>Clustercount, + 1 nunca puede superar FFFFFFF6h.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo Clustercount,.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(Clustercount, + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((clustercount, + 2) * 4)</td>
<td><p>Este campo es obligatorio y su contenido, si existe, no está definido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos Clustercount,, FatLength y BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 \[ campo FatEntry 0 \]

El \[ campo FatEntry 0 \] debe describir el tipo de medio en el primer byte (byte de orden más bajo) y debe contener FFH en los tres bytes restantes.

El tipo de medio (el primer byte) debe ser F8h.

#### <a name="412-fatentry1-field"></a>campo 4.1.2 FatEntry \[ 1 \]

El \[ campo FatEntry 1 \] solo existe debido a la prioridad histórica y no describe nada de interés.

El valor válido para este campo es FFFFFFFFh. Las implementaciones inicializarán este campo en su valor prescrito y no deben usar este campo para ningún propósito. Las implementaciones no deben interpretar este campo y conservarán su contenido entre las operaciones que modifican los campos circundantes.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... FatEntry \[ clustercount, + 1 \]

Cada campo FatEntry de esta matriz representará un clúster en el montón del clúster. FatEntry \[ 2 \] representa el primer clúster del montón del clúster y FatEntry \[ clustercount, + 1 \] representa el último clúster del montón del clúster.

El intervalo válido de valores para estos campos será:

- Entre 2 y Clustercount, + 1, ambos incluidos, que señala a la siguiente FatEntry de la cadena de clúster especificada; el FatEntry determinado no debe apuntar a ningún FatEntry que lo preceda en la cadena de clúster especificada.

- Exactamente FFFFFFF7h, que marca el clúster correspondiente del FatEntry determinado como "malo"

- Exactamente FFFFFFFFh, que marca el clúster correspondiente del FatEntry determinado como el último clúster de una cadena de clústeres. Este es el único valor válido para el último FatEntry de cualquier cadena de clúster determinada.

## <a name="5-data-region"></a>5 regiones de datos

La región de datos contiene el montón del clúster, que proporciona espacio administrado para estructuras, directorios y archivos del sistema de archivos.

### <a name="51-cluster-heap-sub-region"></a>5,1 subregión del montón del clúster

La estructura del montón del clúster es muy simple (vea la [tabla 12](#table-12-cluster-heap-structure)); cada serie consecutiva de sectores describe un clúster, tal y como se define en el campo SectorsPerClusterShift. Lo importante es que el primer clúster del montón del clúster tiene el índice dos, que se corresponde directamente con el índice de FatEntry \[ 2 \] .

En un volumen de exFAT, un mapa de bits de asignación (consulte la [sección 7.1.5](#715-allocation-bitmap)) mantiene el registro del estado de asignación de todos los clústeres. Esta es una diferencia significativa de las predecesoras de exFAT (FAT12, FAT16 y FAT32), en las que una FAT mantiene un registro del estado de asignación de todos los clústeres en el montón del clúster.

<div id="table-12-cluster-heap-structure" />

**Tabla 12 estructura del montón del clúster**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>organismos</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>sector</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Clúster [2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Este campo es obligatorio y la <a href="#511-cluster2--clusterclustercount1-fields">sección 5.1.1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos ClusterHeapOffset y SectorsPerClusterShift.</p></td>
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
<td>Clúster [Clustercount, + 1]</td>
<td>ClusterHeapOffset + (Clustercount,-1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Este campo es obligatorio y la <a href="#511-cluster2--clusterclustercount1-fields">sección 5.1.1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen los campos Clustercount,, ClusterHeapOffset y SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ 2 \] ... Campos de clustercount, de clúster \[ + 1 \]

Cada campo de clúster de esta matriz es una serie de sectores contiguos, cuyo tamaño está definido por el campo SectorsPerClusterShift.

## <a name="6-directory-structure"></a>6 estructura de directorios

El sistema de archivos exFAT utiliza un enfoque de árbol de directorios para administrar las estructuras y los archivos del sistema de archivos que existen en el montón del clúster. Los directorios tienen una relación de uno a varios entre el elemento primario y el secundario en el árbol de directorios.

El directorio al que hace referencia el campo FirstClusterOfRootDirectory es la raíz del árbol de directorios. Todos los demás directorios descienden del directorio raíz en un modo vinculado individualmente.

Cada directorio consta de una serie de entradas de directorio (vea la [Tabla 13](#table-13-directory-structure)).

Una o varias entradas de directorio se combinan en un conjunto de entradas de directorio que describe algo de interés, como una estructura del sistema de archivos, un subdirectorio o un archivo.

<div id="table-13-directory-structure" />

**Tabla 13 estructura de directorios**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry [0]</td>
<td>0</td>
<td>32</td>
<td>Este campo es obligatorio y la <a href="#61-directoryentry0--directoryentryn--1">sección 6,1</a> define su contenido.</td>
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
<td>DirectoryEntry [N – 1]</td>
<td>(N – 1) * 32</td>
<td>32</td>
<td><p>Este campo es obligatorio y la <a href="#61-directoryentry0--directoryentryn--1">sección 6,1</a> define su contenido.</p>
<p>N, el número de campos DirectoryEntry, es el tamaño, en bytes, de la cadena de clúster que contiene el directorio dado, dividido por el tamaño de un campo DirectoryEntry, 32 bytes.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6,1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Cada campo DirectoryEntry de esta matriz se deriva de la plantilla DirectoryEntry genérica (consulte la [sección 6,2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>6,2 plantilla DirectoryEntry genérica

La plantilla DirectoryEntry genérico proporciona la definición base para las entradas de directorio (vea la [Tabla 14](#table-14-generic-directoryentry-template)). Todas las estructuras de entradas de directorio se derivan de esta plantilla y solo son válidas las estructuras de entradas de directorio definidas por Microsoft (exFAT no tiene disposiciones para las estructuras de entradas de directorio definidas por el fabricante excepto según se define en la [sección 7,8](#78-vendor-extension-directory-entry) y en la [sección 7,9](#79-vendor-allocation-directory-entry)). La capacidad de interpretar la plantilla DirectoryEntry genérica es obligatoria.

<div id="table-14-generic-directoryentry-template" />

**Tabla 14 plantilla DirectoryEntry genérica**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#621-entrytype-field">sección 6.2.1</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#622-firstcluster-field">sección 6.2.2</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#623-datalength-field">sección 6.2.3</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 el campo de EntryType

El campo EntryType tiene tres modos de uso que define el valor del campo (vea la lista siguiente).

- 00H, que es un marcador de fin de directorio y se aplican las siguientes condiciones:

  - El resto de campos del DirectoryEntry dado están realmente reservados

  - Todas las entradas de directorio subsiguientes en el directorio especificado también son marcadores de fin de directorio

  - Los marcadores de fin de directorio solo son válidos fuera de los conjuntos de entradas de directorio

  - Las implementaciones pueden sobrescribir los marcadores de fin de directorio según sea necesario

- Entre 01h y 7Fh, que es un marcador de entrada de directorio no utilizado y se aplican las condiciones siguientes:

  - El resto de campos del DirectoryEntry dado están realmente sin definir.

  - Las entradas de directorio no utilizadas solo son válidas fuera de los conjuntos de entradas de directorio

  - Las implementaciones pueden sobrescribir las entradas de directorio no utilizadas según sea necesario

  - Este intervalo de valores corresponde al campo InUse (vea la [sección 6.2.1.4](#6214-inuse-field)) que contiene el valor 0

- Entre 81h y FFh, que es una entrada de directorio normal y se aplican las condiciones siguientes:

  - El contenido del campo EntryType (vea la [tabla 15](#table-15-generic-entrytype-field-structure)) determina el diseño del resto de la estructura DirectoryEntry.

  - Este intervalo de valores, y solo este intervalo de valores, son válidos dentro de un conjunto de entradas de directorio

  - Este intervalo de valores se corresponde directamente con el campo InUse (vea la [sección 6.2.1.4](#6214-inuse-field)) que contiene el valor 1.

Para evitar modificaciones en el campo InUse (consulte la [sección 6.2.1.4](#6214-inuse-field)) de forma errónea, lo que da como resultado un marcador de fin de directorio, el valor 80h no es válido.

<div id="table-15-generic-entrytype-field-structure" />

**Tabla 15 estructura de campo EntryType genérica**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Este campo es obligatorio y la <a href="#6211-typecode-field">sección 6.2.1.1</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#6213-typecategory-field">sección 6.2.1.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#6214-inuse-field">sección 6.2.1.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 campo TypeCode

El campo TypeCode describe parcialmente el tipo específico de la entrada de directorio especificada. Este campo, más los campos TypeImportance y TypeCategory (vea la [sección 6.2.1.2](#6212-typeimportance-field) y [6.2.1.3](#6213-typecategory-field), respectivamente) identifican de forma única el tipo de la entrada de directorio especificada.

Todos los valores posibles de este campo son válidos, a menos que los campos TypeImportance y TypeCategory contengan el valor 0; en ese caso, el valor 0 no es válido para este campo.

##### <a name="6212-typeimportance-field"></a>6.2.1.2 TypeImportance

El campo TypeImportance debe describir la importancia de la entrada de directorio especificada.

Los valores válidos para este campo serán:

- 0, lo que significa que la entrada de directorio dada es crítica (consulte la [sección 6.3.1.2.1](#63121-critical-primary-directory-entries) y la [sección 6.4.1.2.1](#64121-critical-secondary-directory-entries) para ver las entradas críticas principales y críticas del directorio secundario, respectivamente)

- 1, lo que significa que la entrada de directorio dada es benigna (consulte la [sección 6.3.1.2.2](#63122-benign-primary-directory-entries) y la [sección 6.4.1.2.2](#64122-benign-secondary-directory-entries) para entradas de directorio secundario benignas y benignas, respectivamente)

##### <a name="6213-typecategory-field"></a>6.2.1.3 TypeCategory

El campo TypeCategory debe describir la categoría de la entrada de directorio especificada.

Los valores válidos para este campo serán:

- 0, que significa que la entrada de directorio especificada es principal (consulte la [sección 6,3](#63-generic-primary-directoryentry-template)).

- 1, lo que significa que la entrada de directorio dada es secundaria (consulte la [sección 6,4](#64-generic-secondary-directoryentry-template)).

##### <a name="6214-inuse-field"></a>6.2.1.4 campo InUse

El campo InUse debe describir si la entrada de directorio especificada está en uso o no.

Los valores válidos para este campo serán:

- 0, que significa que la entrada de directorio especificada no está en uso. Esto significa que la estructura especificada realmente es una entrada de directorio no usada

- 1, lo que significa que la entrada de directorio especificada está en uso. Esto significa que la estructura especificada es una entrada de directorio normal.

#### <a name="622-firstcluster-field"></a>6.2.2 campo FirstCluster

El campo FirstCluster debe contener el índice del primer clúster de una asignación en el montón del clúster asociado a la entrada de directorio especificada.

El intervalo válido de valores para este campo debe ser:

- Exactamente 0, lo que significa que no existe ninguna asignación de clúster

- Entre 2 y Clustercount, + 1, que es el intervalo de índices de clúster válidos

Las estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH, si una asignación de clúster no es compatible con la estructura derivada.

#### <a name="623-datalength-field"></a>Campo 6.2.3 DATALENGTH

El campo DATALENGTH describe el tamaño, en bytes, de los datos que contiene la asignación de clúster asociada.

El intervalo válido de valor para este campo es:

- Al menos 0; Si el campo FirstCluster contiene el valor 0, el único valor válido de este campo es 0.

- A lo sumo Clustercount, \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Las estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH, si no es posible una asignación de clúster para la estructura derivada.

### <a name="63-generic-primary-directoryentry-template"></a>6,3 plantilla DirectoryEntry principal genérica

La primera entrada de directorio en un conjunto de entradas de directorio debe ser una entrada de directorio principal. Todas las entradas de directorio subsiguientes, si las hay, en el conjunto de entradas de directorio serán entradas de directorio secundario (consulte la [sección 6,4](#64-generic-secondary-directoryentry-template)).

La capacidad de interpretar la plantilla DirectoryEntry principal genérica es obligatoria.

Todas las estructuras de entradas de directorio principales derivan de la plantilla DirectoryEntry principal genérica (vea la [tabla 16](#table-16-generic-primary-directoryentry-template)), que deriva de la plantilla DirectoryEntry genérica (consulte la [sección 6,2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tabla 16 plantilla DirectoryEntry principal genérica**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y en la <a href="#631-entrytype-field">sección 6.3.1</a> se define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#632-secondarycount-field">sección 6.3.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#633-setchecksum-field">sección 6.3.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#634-generalprimaryflags-field">sección 6.3.4</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#635-firstcluster-field">sección 6.3.5</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#636-datalength-field">sección 6.3.6</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérico (consulte la [sección 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>6.3.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérico (consulte la [sección 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>6.3.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 entradas críticas del directorio principal

Las entradas críticas del directorio principal contienen información que es fundamental para la administración adecuada de un volumen exFAT. Solo el directorio raíz contiene entradas de directorio principales críticas (las entradas del directorio de archivos son una excepción, consulte la [sección 7,4](#74-file-directory-entry)).

La definición de las entradas críticas del directorio principal se correlaciona con el número de revisión de exFAT principal. Las implementaciones de deben admitir todas las entradas de directorio principales críticas y solo registrarán las estructuras críticas de entrada de directorio principal que define esta especificación.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 entradas de directorio principal benignas

Las entradas de directorio principal benignas contienen información adicional que puede ser útil para administrar un volumen exFAT. Cualquier directorio puede contener entradas de directorio principales benignas.

La definición de entradas de directorio principales benignas se correlaciona con el número de revisión de exFAT secundario. La compatibilidad con cualquier entrada de directorio principal benigna esta especificación, o cualquier especificación subsiguiente, define es opcional. Una entrada de directorio principal benigna no reconocida representa el conjunto completo de entradas de directorio como desconocido (más allá de la definición de las plantillas de entrada de directorio aplicables).

##### <a name="6313-typecategory-field"></a>6.3.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.3](#6213-typecategory-field)).

Para esta plantilla, el valor válido para este campo debe ser 0.

##### <a name="6314-inuse-field"></a>6.3.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>6.3.2 campo SecondaryCount

El campo SecondaryCount debe describir el número de entradas del directorio secundario que siguen inmediatamente a la entrada de directorio principal especificada. Estas entradas de directorio secundario, junto con la entrada de directorio principal especificada, constituyen el conjunto de entradas de directorio.

El intervalo válido de valores para este campo debe ser:

- Al menos 0, lo que significa que esta entrada de directorio principal es la única entrada en el conjunto de entradas de directorio

- A lo sumo 255, lo que significa que las siguientes entradas de directorio 255 y esta entrada de directorio principal constituyen el conjunto de entradas de directorio

Las estructuras de entradas de directorio principales críticas que se derivan de esta plantilla pueden volver a definir los campos SecondaryCount y Setchecksum (.

#### <a name="633-setchecksum-field"></a>6.3.3 Setchecksum (

El campo Setchecksum (contendrá la suma de comprobación de todas las entradas de directorio en el conjunto de entradas de directorio especificado. Sin embargo, la suma de comprobación excluye este campo (vea la [figura 2](#figure-2-entrysetchecksum-computation)). Las implementaciones comprobarán que el contenido de este campo es válido antes de usar cualquier otra entrada de directorio en el conjunto de entradas de directorio especificado.

Las estructuras de entradas de directorio principales críticas que se derivan de esta plantilla pueden volver a definir los campos SecondaryCount y Setchecksum (.

<div id="figure-2-entrysetchecksum-computation" />

**Figura 2 cálculo de EntrySetChecksum**

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

#### <a name="634-generalprimaryflags-field"></a>6.3.4 GeneralPrimaryFlags

El campo GeneralPrimaryFlags contiene marcas (vea la [Tabla 17](#table-17-generic-generalprimaryflags-field-structure)).

Las estructuras de entradas de directorio principales críticas que se derivan de esta plantilla pueden volver a definir este campo.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabla 17 estructura de campos de GeneralPrimaryFlags genéricos**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#6341-allocationpossible-field">sección 6.3.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#6342-nofatchain-field">sección 6.3.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla pueden definir este campo.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 AllocationPossible

El campo AllocationPossible debe describir si es posible una asignación en el montón del clúster para la entrada de directorio especificada.

Los valores válidos para este campo serán:

- 0, que significa que no es posible una asignación asociada de clústeres y que los campos FirstCluster y DATALENGTH no estén definidos realmente (las estructuras que se derivan de esta plantilla pueden volver a definir esos campos)

- 1, lo que significa que es posible una asignación de clústeres asociada y los campos FirstCluster y DATALENGTH son los definidos

##### <a name="6342-nofatchain-field"></a>6.3.4.2 NoFatChain

El campo NoFatChain debe indicar si la FAT activa describe o no la cadena de clúster de la asignación determinada.

Los valores válidos para este campo serán:

- 0, que significa que las entradas FAT correspondientes para la cadena de clúster de la asignación son válidas y las implementaciones las interpretarán. Si el campo AllocationPossible contiene el valor 0, o si el campo AllocationPossible contiene el valor 1 y el campo FirstCluster contiene el valor 0, el único valor válido de este campo es 0.

- 1, que significa que la asignación asociada es una serie contigua de clústeres; las entradas FAT correspondientes para los clústeres no son válidas y las implementaciones no las interpretan. las implementaciones pueden usar la siguiente ecuación para calcular el tamaño de la asignación asociada: DATALENGTH/(2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) redondeada al entero más próximo.

Si las estructuras de entrada de directorio principal críticas que derivan de esta plantilla vuelven a definir el campo GeneralPrimaryFlags, las entradas FAT correspondientes para cualquier cadena de clúster de asignación asociada son válidas.

#### <a name="635-firstcluster-field"></a>6.3.5 FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.2](#622-firstcluster-field)).

Si el bit NoFatChain es 1, FirstCluster debe apuntar a un clúster válido en el montón del clúster.

Las estructuras de entradas de directorio principales críticas que se derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH. Otras estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH solo si el campo AllocationPossible contiene el valor 0.

#### <a name="636-datalength-field"></a>Campo 6.3.6 DATALENGTH

El campo DATALENGTH debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.3](#623-datalength-field)).

Si el bit NoFatChain es 1, DATALENGTH no debe ser cero. Si el campo FirstCluster es cero, DATALENGTH también debe ser cero.

Las estructuras de entradas de directorio principales críticas que se derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH. Otras estructuras que derivan de esta plantilla pueden volver a definir los campos FirstCluster y DATALENGTH solo si el campo AllocationPossible contiene el valor 0.

### <a name="64-generic-secondary-directoryentry-template"></a>6,4 plantilla DirectoryEntry secundaria genérica

El propósito central de las entradas del directorio secundario es proporcionar información adicional sobre un conjunto de entradas de directorio. La capacidad de interpretar la plantilla DirectoryEntry secundaria genérica es obligatoria.

La definición de las entradas de directorio secundarias críticas y benignas se correlaciona con el número de revisión de exFAT secundario. La compatibilidad con cualquier entrada de directorio secundario crítica o benigna esta especificación, o las especificaciones posteriores, define es opcional.

Todas las estructuras de entradas de directorio secundarias se derivan de la plantilla DirectoryEntry secundaria genérica (vea la [Tabla 18](#table-18-generic-secondary-directoryentry-template)), que deriva de la plantilla DirectoryEntry genérica (consulte la [sección 6,2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabla 18 plantilla DirectoryEntry secundaria genérica**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la sección <a href="#641-entrytype-field">6.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#642-generalsecondaryflags-field">sección 6.4.2</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#643-firstcluster-field">sección 6.4.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#644-datalength-field">sección 6.4.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérico (consulte la [sección 6.2.1](#621-entrytype-field))

##### <a name="6411-typecode-field"></a>6.4.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérico (consulte la [sección 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>6.4.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 entradas de directorio secundario críticas

Las entradas críticas del directorio secundario contienen información que es fundamental para la administración adecuada de su conjunto de entradas de directorio contenedor.
Aunque la compatibilidad con una entrada de directorio secundario crítica específica es opcional, una entrada de directorio crítica no reconocida representa el conjunto completo de entradas de directorio como no reconocido (más allá de la definición de las plantillas de entrada de directorio aplicables).

Sin embargo, si un conjunto de entradas de directorio contiene al menos una entrada de directorio secundario crítica que no reconoce una implementación, la implementación tendrá, como máximo, las plantillas de las entradas de directorio en el conjunto de entradas de directorio, y no los datos de ninguna asignación asociada a ninguna entrada de directorio del conjunto de entradas de directorio (las entradas de directorio de archivos son una excepción; vea la [7,4 sección](#74-file-directory-entry)

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 entradas de directorio secundario benignas

Las entradas de directorio secundario benignas contienen información adicional que puede ser útil para administrar su conjunto de entradas de directorio contenedor. La compatibilidad con cualquier entrada de directorio secundario benigna específica es opcional.
Las entradas de directorio secundario benignas no reconocidas no representan el conjunto de entradas de directorio completo como no reconocido.

Las implementaciones pueden omitir cualquier entrada secundaria benigna que no reconozca.

##### <a name="6413-typecategory-field"></a>6.4.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.3](#6213-typecategory-field)).

Para esta plantilla, el valor válido para este campo es 1.

##### <a name="6414-inuse-field"></a>6.4.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 campo GeneralSecondaryFlags

El campo GeneralSecondaryFlags contiene marcas (vea la [tabla 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabla 19 estructura de campos GeneralSecondaryFlags genéricos**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#6421-allocationpossible-field">sección 6.4.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#6422-nofatchain-field">sección 6.4.2.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Este campo es obligatorio y las estructuras que derivan de esta plantilla pueden definir este campo.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 AllocationPossible

El campo AllocationPossible debe tener la misma definición que el campo con el mismo nombre en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.4.1](#6341-allocationpossible-field)).

##### <a name="6422-nofatchain-field"></a>6.4.2.2 NoFatChain

El campo NoFatChain debe tener la misma definición que el campo con el mismo nombre en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.4.2](#6342-nofatchain-field)).

#### <a name="643-firstcluster-field"></a>6.4.3 campo FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.2](#622-firstcluster-field)).

Si el bit NoFatChain es 1, FirstCluster debe apuntar a un clúster válido en el montón del clúster.

#### <a name="644-datalength-field"></a>Campo 6.4.4 DATALENGTH

El campo DATALENGTH debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry genérica (consulte la [sección 6.2.3](#623-datalength-field)).

Si el bit NoFatChain es 1, DATALENGTH no debe ser cero. Si el campo FirstCluster es cero, DATALENGTH también debe ser cero.

## <a name="7-directory-entry-definitions"></a>7 definiciones de entradas de directorio

La revisión 1,00 del sistema de archivos exFAT define las siguientes entradas de directorio:

- Principal crítico

  - Mapa de bits de asignación ([sección 7,1](#71-allocation-bitmap-directory-entry))

  - Tabla de casos de uso ([sección 7,2](#72-up-case-table-directory-entry))

  - Etiqueta de volumen ([sección 7,3](#73-volume-label-directory-entry))

  - Archivo ([sección 7,4](#74-file-directory-entry))

- Principal benigno

  - GUID de volumen ([sección 7,5](#75-volume-guid-directory-entry))

  - TexFAT padding ([sección 7,10](#710-texfat-padding-directory-entry))

<!-- -->

- Secundaria crítica

  - Extensión de secuencia ([sección 7,6](#76-stream-extension-directory-entry))

  - Nombre de archivo ([sección 7,7](#77-file-name-directory-entry))

- Secundaria benigna

  - Extensión de proveedor ([sección 7,8](#78-vendor-extension-directory-entry))

  - Asignación de proveedor ([sección 7,9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7,1 entrada de directorio de mapa de bits de asignación

En el sistema de archivos exFAT, una FAT no describe el estado de asignación de los clústeres; en su lugar, se realiza un mapa de bits de asignación. Los mapas de bits de asignación existen en el montón del clúster (consulte la [sección 7.1.5](#715-allocation-bitmap)) y tienen las entradas de directorio principal críticas correspondientes en el directorio raíz (vea la [Tabla 20](#table-20-allocation-bitmap-directoryentry-structure)).

El campo NumberOfFats determina el número de entradas válidas del directorio de mapas de bits de asignación en el directorio raíz. Si el campo NumberOfFats contiene el valor 1, el único número válido de entradas de directorio de mapa de bits de asignación es 1. Además, la entrada de directorio de mapa de bits de asignación solo es válida si describe el primer mapa de bits de asignación (consulte la [sección 7.1.2.1](#7121-bitmapidentifier-field)). Si el campo NumberOfFats contiene el valor 2, el único número válido de entradas de directorio de mapa de bits de asignación es 2.
Además, las dos entradas de directorio de mapa de bits de asignación solo son válidas si una describe el primer mapa de bits de asignación y la otra describe el segundo mapa de bits de asignación.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabla 20 mapa de bits de asignación DirectoryEntry (estructura)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#711-entrytype-field">sección 7.1.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#712-bitmapflags-field">sección 7.1.2</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#713-firstcluster-field">sección 7.1.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#714-datalength-field">sección 7.1.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1](#631-entrytype-field)).

##### <a name="7111-typecode-field"></a>7.1.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.1](#6311-typecode-field)).

En el caso de una entrada de directorio de mapa de bits de asignación, el valor válido para este campo es 1.

##### <a name="7112-typeimportance-field"></a>Campo 7.1.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.2](#6312-typeimportance-field)).

En el caso de una entrada de directorio de mapa de bits de asignación, el valor válido para este campo es 0.

##### <a name="7113-typecategory-field"></a>7.1.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.3](#6313-typecategory-field)).

##### <a name="7114-inuse-field"></a>7.1.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.4](#6314-inuse-field)).

#### <a name="712-bitmapflags-field"></a>7.1.2 campo BitmapFlags

El campo BitmapFlags contiene marcas (vea la [tabla 21](#table-21-bitmapflags-field-structure)).

<div id="table-21-bitmapflags-field-structure" />

**Tabla 21 BitmapFlags estructura de campo**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#7121-bitmapidentifier-field">sección 7.1.2.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>1</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 BitmapIdentifier

El campo BitmapIdentifier indicará el mapa de bits de asignación que se describe en la entrada de directorio especificada. Las implementaciones utilizarán el primer mapa de bits de asignación junto con la primera FAT y usarán el segundo mapa de bits de asignación junto con la segunda FAT. El campo ActiveFat describe qué mapa de bits de asignación y FAT están activos.

Los valores válidos para este campo serán:

- 0, que significa que la entrada de directorio dada describe el primer mapa de bits de asignación

- 1, lo que significa que la entrada de directorio dada describe el segundo mapa de bits de asignación y solo es posible cuando NumberOfFats contiene el valor 2

#### <a name="713-firstcluster-field"></a>7.1.3 campo FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.5](#635-firstcluster-field)).

Este campo contiene el índice del primer clúster de la cadena de clústeres, como se describe en la FAT, que hospeda el mapa de bits de asignación.

#### <a name="714-datalength-field"></a>Campo 7.1.4 DATALENGTH

El campo de clúster de meta6.3.6 debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección](#636-datalength-field)).

#### <a name="715-allocation-bitmap"></a>Mapa de bits de asignación de 7.1.5

Un mapa de bits de asignación registra el estado de asignación de los clústeres en el montón del clúster. Cada bit de un mapa de bits de asignación indica si su clúster correspondiente está disponible para su asignación o no.

Un mapa de bits de asignación representa los clústeres del índice más bajo al más alto (vea la [tabla 22](#table-22-allocation-bitmap-structure)). Por motivos históricos, el primer clúster tiene el índice 2.
Nota: el primer bit del mapa de bits es el bit de orden inferior del primer byte.

<div id="table-22-allocation-bitmap-structure" />

**Tabla 22 estructura de mapa de bits de asignación**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry [2]</td>
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
<td>BitmapEntry [Clustercount, + 1]</td>
<td>Clustercount,-1</td>
<td>1</td>
<td><p>Este campo es obligatorio y la <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">sección 7.1.5.1</a> define su contenido.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo Clustercount,.</p></td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>Clustercount,</td>
<td>(DATALENGTH * 8): Clustercount,</td>
<td><p>Este campo es obligatorio y su contenido, si existe, está reservado.</p>
<p>Nota: los sectores principal y de arranque de copia de seguridad contienen el campo Clustercount,.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... BitmapEntry \[ clustercount, + 1 \]

Cada campo BitmapEntry de esta matriz representa un clúster en el montón del clúster. BitmapEntry \[ 2 \] representa el primer clúster del montón del clúster y BitmapEntry \[ clustercount, + 1 \] representa el último clúster del montón del clúster.

Los valores válidos para estos campos serán:

- 0, que describe el clúster correspondiente como disponible para la asignación

- 1, que describe el clúster correspondiente como no disponible para la asignación (una asignación de clúster ya puede consumir el clúster correspondiente o la FAT activa puede describir el clúster correspondiente como incorrecto)

### <a name="72-up-case-table-directory-entry"></a>7,2 entrada de directorio de tabla de casos de uso

La tabla de mayúsculas y minúsculas define la conversión de minúsculas a caracteres en mayúsculas. Esto es importante debido a la entrada del directorio de nombres de archivo (consulte la sección 7,7) uso de caracteres Unicode y el sistema de archivos exFAT no distingue mayúsculas de minúsculas y se conservan las mayúsculas y minúsculas. La tabla de casos de arriba existe en el montón del clúster (vea la [sección 7.2.5](#725-up-case-table)) y tiene una entrada de directorio principal crítica correspondiente en el directorio raíz (vea la [tabla 23](#table-23-up-case-table-directoryentry-structure)). El número válido de entradas de directorio de tabla de casos de uso es 1.

Debido a la relación entre la tabla de casos y los nombres de archivo, las implementaciones no deben modificar la tabla de casos de uso, excepto como resultado de operaciones de formato.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tabla 23: estructura DirectoryEntry de la tabla de casos**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#721-entrytype-field">sección 7.2.1</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#722-tablechecksum-field">sección 7.2.2</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#723-firstcluster-field">sección 7.2.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#724-datalength-field">sección 7.2.4</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 (campo de EntryType)

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1](#631-entrytype-field)).

##### <a name="7211-typecode-field"></a>Campo TypeCode de 7.2.1.1

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.1](#6311-typecode-field)).

Para la entrada de directorio de la tabla de casos de uso, el valor válido para este campo es
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 TypeImportance campo

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.2](#6312-typeimportance-field)).

Para la entrada de directorio de la tabla de casos de uso, el valor válido para este campo es
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.3](#6313-typecategory-field)).

##### <a name="7214-inuse-field"></a>7.2.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.4](#6314-inuse-field)).

#### <a name="722-tablechecksum-field"></a>7.2.2 TableChecksum

El campo TableChecksum contiene la suma de comprobación de la tabla de casos de uso (que describen los campos FirstCluster y DATALENGTH). Las implementaciones deben comprobar que el contenido de este campo es válido antes de usar la tabla de casos de uso.

<div id="figure-3-tablechecksum-computation" />

**Figura 3 cálculo de TableChecksum**

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

#### <a name="723-firstcluster-field"></a>7.2.3 campo FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.5](#635-firstcluster-field)).

Este campo contiene el índice del primer clúster de la cadena de clústeres, como se describe en la FAT, que hospeda la tabla de casos de uso.

#### <a name="724-datalength-field"></a>Campo de longitud de DATALENGTH 7.2.4

El campo de clúster de meta6.3.6 debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección](#636-datalength-field)).

#### <a name="725-up-case-table"></a>7.2.5: tabla de casos

Una tabla con mayúsculas y minúsculas es una serie de asignaciones de caracteres Unicode. Una asignación de caracteres consta de un campo de 2 bytes, con el índice del campo en la tabla de casos de uso de mayúsculas que representa el carácter Unicode que se va a convertir en mayúsculas y el campo de 2 bytes que representa el carácter Unicode con mayúsculas y minúsculas.

Los primeros 128 caracteres Unicode tienen asignaciones obligatorias (consulte la [tabla 24](#table-24-mandatory-first-128-up-case-table-entries)).
Una tabla de mayúsculas y minúsculas que tiene cualquier otra asignación de caracteres para cualquiera de los primeros 128 caracteres Unicode no es válida.

Las implementaciones que solo admiten caracteres del intervalo de asignación obligatorio pueden omitir las asignaciones del resto de la tabla de casos de uso. Estas implementaciones solo usarán caracteres del intervalo de asignación obligatorio al crear o cambiar el nombre de archivos (a través de la entrada del directorio de nombres de archivo, consulte la [sección 7,7](#77-file-name-directory-entry)). Cuando se usan mayúsculas y minúsculas en los nombres de archivo existentes, tales implementaciones no deben poner en mayúsculas los caracteres del intervalo de asignación no obligatorio, pero deben dejarlos intactos en el nombre de archivo con mayúsculas y minúsculas resultante (se trata de un carácter de mayúsculas y minúsculas parcial). Al comparar los nombres de archivo, estas implementaciones tratarán los nombres de archivo que se diferencian del nombre en comparación únicamente por los caracteres Unicode del intervalo de asignación no obligatorio como equivalentes. Aunque estos nombres de archivo solo son potencialmente equivalentes, estas implementaciones no pueden garantizar que el nombre de archivo con mayúsculas y minúsculas no entre en conflicto con el nombre en comparación.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabla 24: primeras 128 entradas de la tabla de casos arriba**

| **Índice de tabla** | **Entradas de tabla** |           |           |           |           |           |           |           |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
|                 | **+ 0**           | **+ 1**   | **+ 2**   | **+ 3**   | **+ 4**   | **+ 5**   | **+ 6**   | **+ 7**   |
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**(Nota: las entradas con asignaciones de mayúsculas y minúsculas que no son de identidad están en negrita)**

Al dar formato a un volumen, las implementaciones pueden generar una tabla de casos de uso en un formato comprimido mediante la compresión de asignación de identidades, ya que una gran parte del espacio de caracteres Unicode no tiene ningún concepto de mayúsculas de minúsculas (lo que significa que los caracteres "en minúscula" y "en mayúscula" son equivalentes).
Las implementaciones comprimen una tabla de mayúsculas y minúsculas representando una serie de asignaciones de identidad con el valor FFFFh seguido del número de asignaciones de identidad.

Por ejemplo, una implementación puede representar las primeras asignaciones de caracteres 100 (64h) con las siguientes ocho entradas de una tabla de casos de uso comprimido:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Las dos primeras entradas indican los primeros 97 caracteres (61h) (de 0000h a 0060h) que tienen asignaciones de identidad. Los caracteres siguientes, 0061h a 0063h, se asignan a los caracteres 0041h a 0043h, respectivamente.

La capacidad de proporcionar una tabla de casos de uso comprimido al formatear un volumen es opcional. Sin embargo, la capacidad de interpretar una tabla sin comprimir y una tabla de casos de uso comprimido es obligatoria. El valor del campo TableChecksum siempre se ajusta al modo en que existe la tabla de casos en el volumen, que puede tener un formato comprimido o sin comprimir.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 la tabla de casos de uso recomendado

Al dar formato a un volumen, las implementaciones de deben registrar la tabla de casos que se recomienda en el formato comprimido (vea la [tabla 25](#table-25-recommended-up-case-table-in-compressed-format)), para la que el valor del campo TableChecksum es E619D30Dh.

Si una implementación define su propia tabla de casos, comprimidos o sin comprimir, esa tabla cubrirá el intervalo de caracteres Unicode completo (de los códigos de carácter 0000h a FFFFh inclusive).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabla 25 se recomienda la tabla de casos en formato comprimido**

| **Desplazamiento sin formato** | **Entradas de tabla comprimida** |         |         |         |         |         |         |         |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
|                | **+ 0**                      | **+ 1** | **+ 2** | **+ 3** | **+ 4** | **+ 5** | **+ 6** | **+ 7** |
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
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
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
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
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
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
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
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
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
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
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
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
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
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
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
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
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
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
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
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

### <a name="73-volume-label-directory-entry"></a>7,3 entrada de directorio de etiqueta de volumen

La etiqueta de volumen es una cadena Unicode que permite a los usuarios finales distinguir sus volúmenes de almacenamiento. En el sistema de archivos exFAT, la etiqueta de volumen existe como una entrada de directorio principal crítica en el directorio raíz (vea la [tabla 26](#table-26-volume-label-directoryentry-structure)). El número válido de entradas de directorio de etiqueta de volumen oscila entre 0 y 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabla 26 etiqueta de volumen DirectoryEntry (estructura)**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#731-entrytype-field">sección 7.3.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#732-charactercount-field">sección 7.3.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Este campo es obligatorio y la <a href="#733-volumelabel-field">sección 7.3.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 (campo de EntryType)

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1](#631-entrytype-field)).

##### <a name="7311-typecode-field"></a>7.3.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.1](#6311-typecode-field)).

Para la entrada de directorio etiqueta de volumen, el valor válido para este campo es
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.2](#6312-typeimportance-field)).

Para la entrada de directorio etiqueta de volumen, el valor válido para este campo es
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.3](#6313-typecategory-field)).

##### <a name="7314-inuse-field"></a>7.3.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.4](#6314-inuse-field)).

#### <a name="732-charactercount-field"></a>7.3.2 CharacterCount

El campo CharacterCount debe contener la longitud de la cadena Unicode que contiene el campo VolumeLabel.

El intervalo válido de valores para este campo debe ser:

- Al menos 0, lo que significa que la cadena Unicode tiene una longitud de 0 caracteres (que equivale a ninguna etiqueta de volumen)

- Como máximo 11, lo que significa que la cadena Unicode tiene 11 caracteres de longitud

#### <a name="733-volumelabel-field"></a>7.3.3 VolumeLabel

El campo VolumeLabel debe contener una cadena Unicode, que es el nombre descriptivo del volumen. El campo VolumeLabel tiene el mismo conjunto de caracteres no válidos que el campo de nombre de archivo de la entrada del directorio de nombres de archivo (consulte la [sección 7.7.3](#773-filename-field)).

### <a name="74-file-directory-entry"></a>Entrada de directorio de archivos 7,4

Las entradas de directorio de archivos describen archivos y directorios. Son entradas de directorio principales críticas y cualquier directorio puede contener cero o más entradas de directorio de archivos (vea la [tabla 27](#table-27-file-directoryentry)). Para que una entrada de directorio de archivos sea válida, exactamente una entrada de directorio de extensión de secuencia y al menos una entrada de directorio de nombre de archivo debe seguir inmediatamente a la entrada de directorio de archivos (vea la [sección 7,6](#76-stream-extension-directory-entry) y la [sección 7,7](#77-file-name-directory-entry), respectivamente).

<div id="table-27-file-directoryentry" />

**Tabla 27 archivo DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#741-entrytype-field">sección 7.4.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#742-secondarycount-field">sección 7.4.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#743-setchecksum-field">sección 7.4.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#744-fileattributes-field">sección 7.4.4</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sección 7.4.6</a> define su contenido.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">sección 7.4.7</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sección 7.4.6</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sección 7.4.6</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">sección 7.4.7</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 (campo de EntryType)

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1](#631-entrytype-field)).

##### <a name="7411-typecode-field"></a>7.4.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.1](#6311-typecode-field)).

En el caso de una entrada de directorio de archivos, el valor válido para este campo es 5.

##### <a name="7412-typeimportance-field"></a>7.4.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.2](#6312-typeimportance-field)).

En el caso de una entrada de directorio de archivos, el valor válido para este campo es 0.

##### <a name="7413-typecategory-field"></a>7.4.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.3](#6313-typecategory-field)).

##### <a name="7414-inuse-field"></a>7.4.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.4](#6314-inuse-field)).

#### <a name="742-secondarycount-field"></a>7.4.2 campo SecondaryCount

El campo SecondaryCount debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.2](#632-secondarycount-field)).

#### <a name="743-setchecksum-field"></a>7.4.3 campo Setchecksum (

El campo Setchecksum (debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.3](#633-setchecksum-field)).

#### <a name="744-fileattributes-field"></a>7.4.4 campo FileAttributes

El campo FileAttributes contiene marcas (vea la [tabla 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**Tabla 28 estructura de campos FileAttributes**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
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

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>7.4.5 CreateTimestamp, Create10msIncrement y CreateUtcOffset

En combinación, los campos CreateTimestamp y CreateTime10msIncrement describirán la fecha y hora local en que se creó el archivo o directorio especificado. El campo CreateUtcOffset describe el desplazamiento de la fecha y hora local con respecto a la hora UTC. Las implementaciones deben establecer estos campos tras la creación del conjunto de entradas de directorio dado.

Estos campos deben ajustarse a las definiciones de los campos timestamp, 10msIncrement y UtcOffset (vea la sección [7.4.8](#748-timestamp-fields), [sección 7.4.9](#749-10msincrement-fields)y la [sección 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>7.4.6 LastModifiedTimestamp, LastModified10msIncrement y LastModifiedUtcOffset

En combinación, los campos LastModifiedTimestamp y LastModifiedTime10msIncrement describirán la fecha y la hora local en que se modificó por última vez el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia determinada. El campo LastModifiedUtcOffset describe el desplazamiento de la fecha y hora local con respecto a la hora UTC. Las implementaciones deben actualizar estos campos:

1. Después de modificar el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia dada (excepto el contenido que existe más allá del punto que describe el campo ValidDataLength)

2. Al cambiar los valores de los campos ValidDataLength o DATALENGTH

Estos campos deben ajustarse a las definiciones de los campos timestamp, 10msIncrement y UtcOffset (vea la sección [7.4.8](#748-timestamp-fields), [sección 7.4.9](#749-10msincrement-fields)y la [sección 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 LastAccessedTimestamp y LastAccessedUtcOffset

El campo LastAccessedTimestamp debe describir la fecha y la hora local a la que se tuvo acceso por última vez al contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de flujo especificada. El campo LastAccessedUtcOffset describe el desplazamiento de la fecha y hora local con respecto a la hora UTC.
Las implementaciones deben actualizar estos campos:

1. Después de modificar el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de secuencia especificada (excepto el contenido que existe más allá de ValidDataLength)

2. Al cambiar los valores de los campos ValidDataLength o DATALENGTH

Las implementaciones deben actualizar estos campos después de leer el contenido de cualquiera de los clústeres asociados a la entrada de directorio de extensión de flujo especificada.

Estos campos deben ajustarse a las definiciones de los campos timestamp y UtcOffset (vea la [sección 7.4.8](#748-timestamp-fields) y la [sección 7.4.10](#7410-utcoffset-fields), respectivamente).

#### <a name="748-timestamp-fields"></a>7.4.8 campos de marca de tiempo

Los campos de marca de tiempo describen la fecha y la hora locales, hasta una resolución de dos segundos (vea la [tabla 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tabla 29 estructura de campos de marca de tiempo**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Este campo es obligatorio y la <a href="#7481-doubleseconds-field">sección 7.4.8.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Minute</td>
<td>5</td>
<td>6</td>
<td>Este campo es obligatorio y la <a href="#7482-minute-field">sección 7.4.8.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Hora</td>
<td>11</td>
<td>5</td>
<td>Este campo es obligatorio y la <a href="#7483-hour-field">sección 7.4.8.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Día</td>
<td>16</td>
<td>5</td>
<td>Este campo es obligatorio y la <a href="#7484-day-field">sección 7.4.8.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>Mes</td>
<td>21</td>
<td>4</td>
<td>Este campo es obligatorio y la <a href="#7485-month-field">sección 7.4.8.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Este campo es obligatorio y la <a href="#7486-year-field">sección 7.4.8.6</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>7.4.8.1 DoubleSeconds

El campo DoubleSeconds debe describir la parte de segundos del campo de marca de tiempo, en múltiplos de dos segundos.

El intervalo válido de valores para este campo debe ser:

- 0, que representa 0 segundos

- 29, que representa 58 segundos

##### <a name="7482-minute-field"></a>7.4.8.2 campo de minuto

El campo minute debe describir la parte de minutos del campo timestamp.

El intervalo válido de valores para este campo debe ser:

- 0, que representa 0 minutos

- 59, que representa 59 minutos

##### <a name="7483-hour-field"></a>7.4.8.3 campo de hora

El campo de hora debe describir la parte de horas del campo de marca de tiempo.

El intervalo válido de valores para este campo debe ser:

- 0, que representa 00:00 horas

- 23, que representa 23:00 horas

##### <a name="7484-day-field"></a>7.4.8.4 campo de día

El campo Day debe describir la parte del día del campo timestamp.

El intervalo válido de valores para este campo debe ser:

- 1, que es el primer día del mes determinado

- El último día del mes dado (el mes dado define el número de días válidos)

##### <a name="7485-month-field"></a>Campo 7.4.8.5 month

El campo month debe describir la parte del mes del campo timestamp.

El intervalo válido de valores para este campo debe ser:

- Al menos 1, que representa el mes de enero

- 12 como máximo, que representa diciembre

##### <a name="7486-year-field"></a>7.4.8.6 campo de año

El campo Year debe describir la parte del año del campo timestamp, relativa al año 1980. Este campo representa el año 1980 con el valor 0 y el año 2107 con el valor 127.

Todos los valores posibles para este campo son válidos.

#### <a name="749-10msincrement-fields"></a>7.4.9 campos 10msIncrement

los campos 10msIncrement deben proporcionar una resolución de tiempo adicional a los campos de marca de tiempo correspondientes en múltiplos de 10 milisegundos.

El intervalo válido de valores para estos campos será:

- Al menos 0, que representa 0 milisegundos

- Como máximo 199, que representa 1990 milisegundos

#### <a name="7410-utcoffset-fields"></a>7.4.10 campos UtcOffset

Los campos de UtcOffset (vea la [Tabla 30](#table-30-utcoffset-field-structure)) describen el desplazamiento desde la hora UTC hasta la fecha y hora locales que describen los campos de marca de tiempo y 10msIncrement correspondientes. El desplazamiento desde la hora UTC hasta la fecha y hora locales incluye los efectos de las zonas horarias y otros ajustes de fecha y hora, como los cambios en el horario de verano regional y el horario de verano.

<div id="table-30-utcoffset-field-structure" />

**Tabla 30 estructura de campos de UtcOffset**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>poco</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>parada</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Este campo es obligatorio y la <a href="#74101-offsetfromutc-field">sección 7.4.10.1</a>define su contenido.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#74102-offsetvalid-field">sección 7.4.10.2</a> define su contenido.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>7.4.10.1 OffsetFromUtc

El campo OffsetFromUtc debe describir el desplazamiento con respecto a la hora UTC de la fecha y hora local que contienen los campos marca de tiempo y 10msIncrement relacionados.
Este campo describe el desplazamiento con respecto a la hora UTC en intervalos de 15 minutos (vea la tabla 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabla 31 significado de los valores del campo OffsetFromUtc**

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
<td>La fecha y hora locales es UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>La fecha y hora locales es UTC + 15:30</td>
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
<td>La fecha y hora locales es UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00H</td>
<td>0</td>
<td>La fecha y hora locales es UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>La fecha y hora locales es UTC – 00:15</td>
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
<td>La fecha y hora locales es UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>La fecha y hora locales es UTC – 16:00</td>
</tr>
</tbody>
</table>

Como indica la tabla anterior, todos los valores posibles para este campo son válidos. Sin embargo, las implementaciones solo deben registrar el valor 00H para este campo cuando:

1. La fecha y hora locales son, en realidad, la misma que la hora UTC, en cuyo caso el valor del campo OffsetValid debe ser 1

2. No se conoce la fecha y hora locales, en cuyo caso el valor del campo OffsetValid debe ser 1 y las implementaciones considerarán UTC como fecha y hora local.

3. No se conoce la hora UTC, en cuyo caso el valor del campo OffsetValid debe ser 0

Si el desplazamiento de fecha y hora local con respecto a la hora UTC no va a ser múltiplo de 15 minutos, las implementaciones registrarán 00H en el campo OffsetFromUtc y considerarán UTC como fecha y hora local.

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 OffsetValid

El campo OffsetValid debe describir si el contenido del campo OffsetFromUtc es válido o no, como se indica a continuación:

- 0, que significa que el contenido del campo OffsetFromUtc no es válido
    > y serán 00H

- 1, lo que significa que el contenido del campo OffsetFromUtc es válido

Las implementaciones solo deben establecer este campo en el valor 0 cuando la hora UTC no está disponible para calcular el valor del campo OffsetFromUtc. Si este campo contiene el valor 0, las implementaciones deben tratar los campos timestamp y 10msIncrement con el mismo desplazamiento UTC que la fecha y hora locales actuales.

### <a name="75-volume-guid-directory-entry"></a>7,5 entrada de directorio GUID de volumen

La entrada de directorio GUID de volumen contiene un GUID que permite a las implementaciones distinguir los volúmenes de forma exclusiva y mediante programación.
El GUID del volumen existe como una entrada de directorio principal benigna en el directorio raíz (vea la [tabla 32](#table-32-volume-guid-directoryentry)). El número válido de entradas de directorio GUID de volumen oscila entre 0 y 1.

<div id="table-32-volume-guid-directoryentry" />

**Tabla 32 metaguid de volumen DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#751-entrytype-field">sección 7.5.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#752-secondarycount-field">sección 7.5.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#753-setchecksum-field">sección 7.5.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#754-generalprimaryflags-field">sección 7.5.4</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#755-volumeguid-field">sección 7.5.5</a> define su contenido.</td>
</tr>
<tr class="even">
<td>Reservado</td>
<td>22</td>
<td>10</td>
<td>Este campo es obligatorio y su contenido está reservado.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1](#631-entrytype-field)).

##### <a name="7511-typecode-field"></a>7.5.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.1](#6311-typecode-field)).

Para la entrada de directorio GUID de volumen, el valor válido para este campo es
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.2](#6312-typeimportance-field)).

Para la entrada de directorio GUID de volumen, el valor válido para este campo es
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.3](#6313-typecategory-field)).

##### <a name="7514-inuse-field"></a>7.5.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.1.4](#6314-inuse-field)).

#### <a name="752-secondarycount-field"></a>7.5.2 campo SecondaryCount

El campo SecondaryCount debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.2](#632-secondarycount-field)).

Para la entrada de directorio GUID de volumen, el valor válido para este campo es
0.

#### <a name="753-setchecksum-field"></a>7.5.3 Setchecksum (

El campo Setchecksum (debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.3](#633-setchecksum-field)).

#### <a name="754-generalprimaryflags-field"></a>7.5.4 campo GeneralPrimaryFlags

El campo GeneralPrimaryFlags debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.4](#634-generalprimaryflags-field)) y define el contenido del campo CustomDefined que se va a reservar.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.4.1](#6341-allocationpossible-field)).

Para la entrada de directorio GUID de volumen, el valor válido para este campo es
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 NoFatChain

El campo NoFatChain debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry principal genérica (consulte la [sección 6.3.4.2](#6342-nofatchain-field)).

#### <a name="755-volumeguid-field"></a>7.5.5 campo VolumeGuid

El campo VolumeGuid debe contener un GUID que identifique de forma única el volumen especificado.

Todos los valores posibles para este campo son válidos, excepto el GUID null, que es {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>7,6 entrada de directorio de extensión de secuencia

La entrada de directorio de extensión de secuencia es una entrada de directorio secundario crítica en conjuntos de entradas del directorio de archivos (vea la [tabla 33](#table-33-stream-extension-directoryentry)). El número válido de entradas de directorio de extensión de secuencia en un conjunto de entradas del directorio de archivos es 1.
Además, esta entrada de directorio solo es válida si sigue inmediatamente a la entrada de directorio de archivos.

<div id="table-33-stream-extension-directoryentry" />

**Tabla 33 de la extensión de secuencia DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#761-entrytype-field">sección 7.6.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#762-generalsecondaryflags-field">sección 7.6.2</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#763-namelength-field">sección 7.6.3</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Este campo es obligatorio y la <a href="#764-namehash-field">sección 7.6.4</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#765-validdatalength-field">sección 7.6.5</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#766-firstcluster-field">sección 7.6.6</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#767-datalength-field">sección 7.6.7</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1](#641-entrytype-field)).

##### <a name="7611-typecode-field"></a>7.6.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.1](#6411-typecode-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 0.

##### <a name="7612-typeimportance-field"></a>7.6.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.2](#6412-typeimportance-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 0.

##### <a name="7613-typecategory-field"></a>7.6.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.3](#6413-typecategory-field)).

##### <a name="7614-inuse-field"></a>7.6.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.4](#6414-inuse-field)).

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 GeneralSecondaryFlags

El campo GeneralSecondaryFlags debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2](#642-generalsecondaryflags-field)) y define el contenido del campo CustomDefined que se va a reservar.

##### <a name="7621-allocationpossible-field"></a>7.6.2.1 AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.1](#6421-allocationpossible-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 1.

##### <a name="7622-nofatchain-field"></a>7.6.2.2 NoFatChain

El campo NoFatChain debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.2](#6422-nofatchain-field)).

#### <a name="763-namelength-field"></a>7.6.3 NameLength

El campo NameLength debe contener la longitud de la cadena Unicode. las entradas subsiguientes del directorio de nombres de archivo (consulte la [sección 7,7](#77-file-name-directory-entry)) contienen colectivamente.

El intervalo válido de valores para este campo debe ser:

- Al menos 1, que es el nombre de archivo más corto posible

- Como máximo, 255, que es el nombre de archivo más largo posible

El valor del campo NameLength también afecta a las entradas de directorio de nombre de archivo de número (consulte la [sección 7,7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>7.6.4 NameHash

El campo NameHash debe contener un hash de 2 bytes (consulte la [figura 4](#figure-4-namehash-computation)) del nombre de archivo con mayúsculas y minúsculas. Esto permite que las implementaciones realicen una comparación rápida al buscar un archivo por su nombre. Lo importante es que NameHash proporciona una comprobación de que no coincide. Las implementaciones comprobarán todas las coincidencias de NameHash con una comparación del nombre de archivo con mayúsculas y minúsculas.

<div id="figure-4-namehash-computation" />

**Figura 4 cálculo de NameHash**

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

#### <a name="765-validdatalength-field"></a>7.6.5 campo ValidDataLength

El campo ValidDataLength debe describir hasta qué punto se han escrito los datos de usuario del flujo de datos. Las implementaciones deben actualizar este campo a medida que escriben datos más en el flujo de datos. En los medios de almacenamiento, los datos entre la longitud de datos válida y la longitud de los datos del flujo de datos son indefinidos. Las implementaciones devolverán ceros para las operaciones de lectura más allá de la longitud de datos válida.

Si la entrada del directorio de archivos correspondiente describe un directorio, el único valor válido para este campo es igual al valor del campo DATALENGTH. De lo contrario, el intervalo de valores válidos para este campo será:

- Al menos 0, lo que significa que no se ha escrito ningún dato de usuario en el flujo de datos

- A lo sumo, lo que significa que los datos de usuario se han escrito en toda la longitud del flujo de datos

#### <a name="766-firstcluster-field"></a>7.6.6 campo FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.3](#643-firstcluster-field)).

Este campo contendrá el índice del primer clúster de la secuencia de datos, que hospeda los datos del usuario.

#### <a name="767-datalength-field"></a>Campo 7.6.7 DATALENGTH

El campo DATALENGTH debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.4](#644-datalength-field)).

Si la entrada de directorio de archivos correspondiente describe un directorio, el valor válido para este campo es el tamaño completo de la asignación asociada, en bytes, que puede ser 0. Además, en el caso de los directorios, el valor máximo de este campo es de 256 MB.

### <a name="77-file-name-directory-entry"></a>7,7 entrada de directorio de nombre de archivo

Las entradas de directorio de nombre de archivo son entradas de directorio secundarias críticas en conjuntos de entradas de directorio de archivos (vea la [tabla 34](#table-34-file-name-directoryentry)). El número válido de entradas del directorio de nombres de archivo en un conjunto de entradas del directorio de archivos es NameLength/15, redondeado al entero más cercano. Además, las entradas de directorio de nombre de archivo solo son válidas si siguen inmediatamente a la entrada de directorio de extensión de secuencia como una serie consecutiva. Entradas de directorio de nombre de archivo se combinan para formar el nombre de archivo del conjunto de entradas del directorio de archivos.

Todos los elementos secundarios de una entrada de directorio determinada tendrán conjuntos de entradas de directorio de nombre de archivo único. Es decir, no puede haber nombres de archivo o directorio duplicados después del uso de mayúsculas y minúsculas en un directorio.

<div id="table-34-file-name-directoryentry" />

**Tabla 34 nombre de archivo DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#771-entrytype-field">sección 7.7.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#772-generalsecondaryflags-field">sección 7.7.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Este campo es obligatorio y la <a href="#773-filename-field">sección 7.7.3</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1](#641-entrytype-field)).

##### <a name="7711-typecode-field"></a>7.7.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.1](#6411-typecode-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 1.

##### <a name="7712-typeimportance-field"></a>7.7.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.2](#6412-typeimportance-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 0.

##### <a name="7713-typecategory-field"></a>7.7.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.3](#6413-typecategory-field)).

##### <a name="7714-inuse-field"></a>7.7.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.4](#6414-inuse-field)).

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 GeneralSecondaryFlags

El campo GeneralSecondaryFlags debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2](#642-generalsecondaryflags-field)) y define el contenido del campo CustomDefined que se va a reservar.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.1](#6421-allocationpossible-field)).

Para la entrada de directorio de la extensión de secuencia, el valor válido para este campo es 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 NoFatChain

El campo NoFatChain debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.2](#6422-nofatchain-field)).

#### <a name="773-filename-field"></a>7.7.3 campo Nombre de archivo

El campo FileName debe contener una cadena Unicode, que es una parte del nombre de archivo. En el orden en que se encuentran las entradas de directorio de nombres de archivo en un conjunto de entradas del directorio de archivos, los campos de nombre de archivo se concatenan para formar el nombre de archivo del conjunto de entradas del directorio de archivos Dada la longitud del campo de nombre de archivo, 15 caracteres y el número máximo de entradas del directorio de nombres de archivo, 17, la longitud máxima del nombre de archivo concatenado final es
255.

El nombre de archivo concatenado tiene el mismo conjunto de caracteres no válidos que otros sistemas de archivos basados en FAT (consulte la [tabla 35](#table-35-invalid-filename-characters)). Las implementaciones deben establecer los caracteres no usados de los campos de nombre de archivo en el valor 0000h.

<div id="table-35-invalid-filename-characters" />

**Tabla 35 caracteres de nombre de archivo no válidos**

| **Código de carácter** | **Descripción** | **Código de carácter** | **Descripción**   | **Código de carácter** | **Descripción** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Código de control    | 0001h              | Código de control      | 0002h              | Código de control    |
| 0003h              | Código de control    | 0004h              | Código de control      | 0005h              | Código de control    |
| 0006h              | Código de control    | 0007h              | Código de control      | 0008h              | Código de control    |
| 0009h              | Código de control    | 000Ah              | Código de control      | 000Bh              | Código de control    |
| 000Ch              | Código de control    | 000Dh              | Código de control      | 000Eh              | Código de control    |
| 000Fh              | Código de control    | 0010h              | Código de control      | 0011h              | Código de control    |
| 0012h              | Código de control    | 0013h              | Código de control      | 0014h              | Código de control    |
| 0015h              | Código de control    | 0016h              | Código de control      | 0017h              | Código de control    |
| 0018h              | Código de control    | 0019h              | Código de control      | 001Ah              | Código de control    |
| 001Bh              | Código de control    | 001Ch              | Código de control      | 001Dh              | Código de control    |
| 001Eh              | Código de control    | 001Fh              | Código de control      | 0022h              | Comillas  |
| 002Ah              | Asterisk        | 002Fh              | Barra diagonal     | 003Ah              | Dos puntos           |
| 003Ch              | Signo de menor que  | 003Eh              | Signo de mayor que | 003Fh              | Signo de interrogación   |
| 005Ch              | Barra diagonal inversa      | 007Ch              | Barra vertical      |                    |                 |

Los nombres de archivo "." y ".." tienen el significado especial de "este directorio" y "directorio contenedor", respectivamente. Las implementaciones no deben registrar ninguno de estos nombres de archivo reservados en el campo Nombre de archivo.
Sin embargo, las implementaciones pueden generar estos dos nombres de archivo en los listados de directorios para hacer referencia al directorio que se muestra y al directorio contenedor.

Es posible que las implementaciones deseen restringir los nombres de archivo y directorio solo al Juego de caracteres ASCII. Si es así, deben limitar el uso de caracteres al intervalo de caracteres válidos en las primeras entradas Unicode 128. Todavía deben almacenar los nombres de archivos y directorios en Unicode en el volumen y convertirse en ASCII/Unicode al interactuar con el usuario.

### <a name="78-vendor-extension-directory-entry"></a>7,8 entrada de directorio de extensión de proveedor

La entrada de directorio de extensión de proveedor es una entrada de directorio secundario benigna en los conjuntos de entradas del directorio de archivos (vea la [tabla 36](#table-36-vendor-extension-directoryentry)). Un conjunto de entradas de directorio de archivos puede contener cualquier número de entradas de directorio de extensión de proveedor, hasta el límite de entradas del directorio secundario, menos el número de entradas del directorio secundario. Además, las entradas de directorio de extensión de proveedor solo son válidas si no preceden a las entradas de directorio de nombre de archivo y extensión de secuencia necesarias.

Las entradas de directorio de extensión de proveedor permiten a los proveedores tener entradas únicas de directorio específicas del proveedor en conjuntos de entradas de directorio de archivos individuales mediante el campo VendorGuid (consulte la [tabla 36](#table-36-vendor-extension-directoryentry)). Las entradas de directorio únicas permiten a los proveedores extender el sistema de archivos exFAT de forma eficaz. Los proveedores pueden definir el contenido del campo VendorDefined (consulte la [tabla 36](#table-36-vendor-extension-directoryentry)). Las implementaciones de proveedor pueden mantener el contenido del campo VendorDefined y pueden proporcionar funcionalidad específica del proveedor.

Las implementaciones que no reconocen el GUID de una entrada de directorio de extensión de proveedor deben tratar la entrada del directorio de la misma forma que cualquier otra entrada de directorio secundario benigna no reconocida (consulte la [sección 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Tabla 36 DirectoryEntry extensión de proveedor**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#781-entrytype-field">sección 7.8.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#782-generalsecondaryflags-field">sección 7.8.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#783-vendorguid-field">sección 7.8.3</a> define su contenido.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Este campo es obligatorio y los proveedores pueden definir su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1](#641-entrytype-field)).

##### <a name="7811-typecode-field"></a>7.8.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.1](#6411-typecode-field)).

Para la entrada de directorio de extensión de proveedor, el valor válido para este campo es 0.

##### <a name="7812-typeimportance-field"></a>7.8.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.2](#6412-typeimportance-field)).

Para la entrada de directorio de extensión de proveedor, el valor válido para este campo es 1.

##### <a name="7813-typecategory-field"></a>7.8.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.3](#6413-typecategory-field)).

##### <a name="7814-inuse-field"></a>7.8.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.4](#6414-inuse-field)).

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 GeneralSecondaryFlags

El campo GeneralSecondaryFlags debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2](#642-generalsecondaryflags-field)) y define el contenido del campo CustomDefined que se va a reservar.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.1](#6421-allocationpossible-field)).

Para la entrada de directorio de extensión de proveedor, el valor válido para este campo es 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 NoFatChain

El campo NoFatChain debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.2](#6422-nofatchain-field)).

#### <a name="783-vendorguid-field"></a>7.8.3 VendorGuid

El campo VendorGuid debe contener un GUID que identifique de forma única la extensión de proveedor especificada.

Todos los valores posibles para este campo son válidos, excepto el GUID null, que es {00000000-0000-0000-0000-000000000000} . Sin embargo, los proveedores deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al definir sus extensiones.

El valor de este campo determina la estructura específica del proveedor del campo VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>7,9 entrada de directorio de asignación de proveedor

La entrada de directorio de asignación de proveedor es una entrada de directorio secundario benigna en los conjuntos de entradas del directorio de archivos (vea la [tabla 37](#table-37-vendor-allocation-directoryentry)). Un conjunto de entradas de directorio de archivos puede contener cualquier número de entradas de directorio de asignación de proveedores, hasta el límite de entradas de directorio secundarias, menos el número de entradas de directorio secundarias. Además, las entradas de directorio de asignación de proveedor solo son válidas si no preceden a las entradas de directorio de nombre de archivo y extensión de secuencia necesarias.

Las entradas de directorio de asignación de proveedores permiten a los proveedores tener entradas de directorio únicas y específicas del proveedor en conjuntos de entradas de directorio de archivos individuales mediante el campo VendorGuid (vea la [tabla 37](#table-37-vendor-allocation-directoryentry)). Las entradas de directorio únicas permiten a los proveedores extender el sistema de archivos exFAT de forma eficaz. Los proveedores pueden definir el contenido de los clústeres asociados, si existen. Las implementaciones de proveedores pueden mantener el contenido de los clústeres asociados, si los hay, y pueden proporcionar funcionalidad específica del proveedor.

Las implementaciones que no reconocen el GUID de una entrada de directorio de asignación de proveedor deben tratar la entrada de directorio igual que cualquier otra entrada de directorio secundaria benigna no reconocida (consulte la [sección 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tabla 37 DirectoryEntry de asignación de proveedor**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType tal y</td>
<td>0</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#791-entrytype-field">sección 7.9.1</a> define su contenido.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Este campo es obligatorio y la <a href="#792-generalsecondaryflags-field">sección 7.9.2</a> define su contenido.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Este campo es obligatorio y la <a href="#793-vendorguid-field">sección 7.9.3</a> define su contenido.</td>
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
<td>Este campo es obligatorio y la <a href="#794-firstcluster-field">sección 7.9.4</a> define su contenido.</td>
</tr>
<tr class="even">
<td>DataLength</td>
<td>24</td>
<td>8</td>
<td>Este campo es obligatorio y la <a href="#795-datalength-field">sección 7.9.5</a> define su contenido.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 campo de EntryType

El campo EntryType debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1](#641-entrytype-field)).

##### <a name="7911-typecode-field"></a>7.9.1.1 campo TypeCode

El campo TypeCode debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.1](#6411-typecode-field)).

Para la entrada de directorio de asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7912-typeimportance-field"></a>7.9.1.2 TypeImportance

El campo TypeImportance debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.2](#6412-typeimportance-field)).

Para la entrada de directorio de asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7913-typecategory-field"></a>7.9.1.3 TypeCategory

El campo TypeCategory debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.3](#6413-typecategory-field)).

##### <a name="7914-inuse-field"></a>7.9.1.4 campo InUse

El campo InUse debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.1.4](#6414-inuse-field)).

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 GeneralSecondaryFlags

El campo GeneralSecondaryFlags debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2](#642-generalsecondaryflags-field)) y define el contenido del campo CustomDefined que se va a reservar.

##### <a name="7921-allocationpossible-field"></a>7.9.2.1 AllocationPossible

El campo AllocationPossible debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.1](#6421-allocationpossible-field)).

Para la entrada de directorio de asignación de proveedor, el valor válido para este campo es 1.

##### <a name="7922-nofatchain-field"></a>7.9.2.2 NoFatChain

El campo NoFatChain debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.2.2](#6422-nofatchain-field)).

#### <a name="793-vendorguid-field"></a>7.9.3 VendorGuid

El campo VendorGuid debe contener un GUID que identifique de forma única la asignación de proveedor especificada.

Todos los valores posibles para este campo son válidos, excepto el GUID null, que es {00000000-0000-0000-0000-000000000000} . Sin embargo, los proveedores deben usar una herramienta de generación de GUID, como GuidGen.exe, para seleccionar un GUID al definir sus extensiones.

El valor de este campo determina la estructura específica del proveedor del contenido de los clústeres asociados, si existe alguno.

#### <a name="794-firstcluster-field"></a>7.9.4 FirstCluster

El campo FirstCluster debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.3](#643-firstcluster-field)).

#### <a name="795-datalength-field"></a>Campo 7.9.5 DATALENGTH

El campo DATALENGTH debe ajustarse a la definición proporcionada en la plantilla DirectoryEntry secundaria genérica (consulte la [sección 6.4.4](#644-datalength-field)).

### <a name="710-texfat-padding-directory-entry"></a>7,10 entrada de directorio TexFAT padding

Esta especificación, la especificación básica del sistema de archivos de la revisión de exFAT 1,00, no define la entrada del directorio TexFAT padding. Sin embargo, el código de tipo es 1 y su importancia de tipo es 1. Las implementaciones de esta especificación deben tratar las entradas de directorio de TexFAT padding iguales que las demás entradas de directorio principal benignas no reconocidas. las implementaciones no moverán las entradas de directorio de relleno de TexFAT.

## <a name="8-implementation-notes"></a>8 notas de implementación

### <a name="81-recommended-write-ordering"></a>8,1 orden de escritura recomendado

Las implementaciones deben asegurarse de que el volumen sea lo más resistente posible a los errores de energía y otros errores inevitables. Al crear nuevas entradas de directorio o modificar las asignaciones de clúster, las implementaciones generalmente deben seguir este orden de escritura:

1. Establezca el valor del campo VolumeDirty en 1

2. Actualizar la FAT activa, si es necesario

3. Actualizar el mapa de bits de asignación activa

4. Crear o actualizar la entrada de directorio, si es necesario

5. Borre el valor del campo VolumeDirty en 0, si su valor antes del primer paso era 0

Al eliminar entradas de directorio o liberar asignaciones de clúster, las implementaciones deben seguir este orden de escritura:

1. Establezca el valor del campo VolumeDirty en 1

2. Eliminar o actualizar la entrada de directorio, si es necesario

3. Actualizar la FAT activa, si es necesario

4. Actualizar el mapa de bits de asignación activa

5. Borre el valor del campo VolumeDirty en 0, si su valor antes del primer paso era 0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8,2 implicaciones de las entradas de directorio no reconocidas

Las especificaciones de exFAT futuras del mismo número de revisión principal, 1 y número de revisión secundaria superior a 0, pueden definir nuevas entradas de directorio secundario benigna principal, crítica secundaria y benigna. Solo las especificaciones de exFAT de un número de revisión mayor superior pueden definir nuevas entradas críticas del directorio principal. Las implementaciones de esta especificación, la especificación básica del sistema de archivos de la revisión de exFAT 1,00, deben ser capaces de montar y acceder a cualquier volumen de exFAT de la revisión principal número 1 y cualquier número de revisión menor. Esto presenta escenarios en los que una implementación puede encontrar entradas de directorio que no reconoce. A continuación se describen las implicaciones de estos escenarios:

1. La presencia de entradas de directorio principal críticas no reconocidas en el directorio raíz representa el volumen no válido. La presencia de cualquier entrada de directorio principal crítica, excepto las entradas de directorio de archivos, en cualquier directorio no raíz, representa el directorio de hospedaje no válido.

2. Las implementaciones no deben modificar las entradas de directorio principal benignas no reconocidas ni las asignaciones de clúster asociadas. Sin embargo, cuando se elimina un directorio y solo cuando se elimina un directorio, las implementaciones eliminarán las entradas de directorio principal benignas no reconocidas y liberarán todas las asignaciones de clúster asociadas, si las hay.

3. Las implementaciones no deben modificar entradas de directorio secundarias críticas no reconocidas ni sus asignaciones de clúster asociadas. La presencia de una o varias entradas de directorio secundaria críticas no reconocidas en un conjunto de entradas de directorio representa todo el conjunto de entradas de directorio no reconocido. Cuando se elimina un conjunto de entradas de directorio que contiene una o varias entradas de directorio secundaria críticas no reconocidas, las implementaciones liberarán todas las asignaciones de clúster, si las hubiera, asociadas a entradas de directorio secundario críticas no reconocidas.
   Además, si el conjunto de entradas de directorio describe un directorio, las implementaciones pueden:

   - Atravesar en el directorio

   - Enumerar las entradas de directorio que contiene

   - Eliminar entradas de directorio contenidas

   - Trasladar entradas de directorio contenidas a un directorio diferente

   Sin embargo, las implementaciones no deben:

   - Modifique las entradas de directorio contenidas, excepto Delete, como se indicó

   - Crear nuevas entradas de directorio contenidas

   - Abrir entradas de directorio contenidas, excepto recorrer y enumerar, como se indicó

4. Las implementaciones no deben modificar entradas de directorio secundarias benignas no reconocidas ni sus asignaciones de clúster asociadas.
   Las implementaciones deben omitir las entradas de directorio secundario benignas no reconocidas. Cuando se elimina un conjunto de entradas de directorio, las implementaciones liberarán todas las asignaciones de clúster, si las hay, asociadas a entradas de directorio secundarias benignas no reconocidas.

## <a name="9-file-system-limits"></a>9 límites del sistema de archivos

### <a name="91-sector-size-limits"></a>9,1 límites de tamaño de sector

El campo BytesPerSectorShift define los límites de tamaño de sector inferior y superior (que se evalúa como **límite inferior: 512 bytes; límite superior: 4.096 bytes**).

### <a name="92-cluster-size-limits"></a>9,2 límites de tamaño de clúster

El campo SectorsPerClusterShift define los límites de tamaño de clúster inferior y superior (**límite inferior: 1 sector; límite superior: 25--BytesPerSectorShift sectores**, que se evalúa en 32 MB).

### <a name="93-cluster-heap-size-limits"></a>9,3 límites de tamaño del montón del clúster

El montón del clúster debe contener al menos espacio suficiente para hospedar las siguientes estructuras básicas del sistema de archivos: el directorio raíz, todos los mapas de bits de asignación y la tabla de casos de uso.

El límite de tamaño del montón de clúster inferior es una función del límite de tamaño inferior de cada una de las estructuras básicas del sistema de archivos que residen en el montón del clúster. Incluso dado el clúster más pequeño posible (512 bytes), cada una de las estructuras básicas del sistema de archivos no necesita más de un clúster. Por lo tanto, el **límite inferior es: 2 + clústeres de NumberOfFats**, que se evalúa en 3 o 4 clústeres, según el valor del campo NumberOfFats.

El límite superior de tamaño del montón del clúster es una función sencilla del máximo número posible de clústeres, que define el campo Clustercount, (**límite superior: 2 <sup>32</sup>-11 clústeres**). Independientemente del tamaño del clúster, este montón de clúster tiene espacio suficiente para hospedar las estructuras básicas del sistema de archivos.

### <a name="94-volume-size-limits"></a>9,4 límites de tamaño de volumen

El campo VolumeLength define los límites de tamaño de volumen inferior y superior (límite inferior: **2 <sup>20</sup>/2 sectores de <sup>BytesPerSectorShift</sup>**, que se evalúa como 1 MB; **límite superior: 2 <sup>64</sup>-1 sectores**, que, dado el mayor tamaño de sector posible, se evalúa en aproximadamente 64ZB). Sin embargo, esta especificación recomienda no tener más<sup>de dos</sup>clústeres en el montón del clúster (consulte la [sección 3.1.9](#319-clustercount-field)). Por lo tanto, el límite superior recomendado de un volumen es: ClusterHeapOffset + (2<sup>24</sup>-2) \* 2<sup>SectorsPerClusterShift</sup>. Dado el tamaño de clúster más grande posible, 32 MB y suponiendo que ClusterHeapOffset es 96MB (espacio suficiente para las regiones de arranque principal y de copia de seguridad y solo la primera FAT), el límite superior recomendado de un volumen se evalúa en aproximadamente 512TB.

### <a name="95-directory-size-limits"></a>9,5 límites de tamaño de directorio

El campo DATALENGTH de la entrada de directorio de la extensión de secuencia define los límites inferior y superior del tamaño del directorio (**límite inferior: 0 bytes; límite superior: 256 MB**). Esto significa que un directorio puede hospedar hasta 8.388.608 entradas de directorio (cada entrada de directorio consume 32 bytes). Dado el menor valor posible del conjunto de entradas del directorio de archivos, un directorio puede hospedar hasta 2.796.202 archivos.

## <a name="10-appendix"></a>10 Apéndice

### <a name="101-globally-unique-identifiers-guids"></a>10,1 identificadores únicos globales (GUID)

Un GUID es la implementación de Microsoft de un identificador único universal. Un GUID es un valor de 128 bits que consta de un grupo de 8 dígitos hexadecimales, seguido de tres grupos de 4 dígitos hexadecimales, seguidos de un grupo de 12 dígitos hexadecimales, por ejemplo {6B29FC40-CA47-1067-B31D-00DD010662DA}, (vea la [tabla 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Tabla 38 estructura de GUID**

<table>
<thead>
<tr class="header">
<th><strong>Nombre del campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>bytes</strong></p></th>
<th><p><strong>Tamaño</strong></p>
<p><strong>bytes</strong></p></th>
<th><strong>Comentarios</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
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
<td>Este campo es obligatorio y contiene los dos bytes del tercer grupo del GUID (1067h del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4 [0]</td>
<td>8</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el byte más significativo del cuarto grupo del GUID (B3h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4 [1]</td>
<td>9</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el byte menos significativo del cuarto grupo del GUID (1Dh del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4 [2]</td>
<td>10</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el primer byte del quinto grupo del GUID (00H del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4 [3]</td>
<td>11</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el segundo byte del quinto grupo del GUID (DDh del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4 [4]</td>
<td>12</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el tercer byte del quinto grupo del GUID (01h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4 [5]</td>
<td>13</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el cuarto byte del quinto grupo del GUID (06h del ejemplo).</td>
</tr>
<tr class="even">
<td>Data4 [6]</td>
<td>14</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el quinto byte del quinto grupo del GUID (62h del ejemplo).</td>
</tr>
<tr class="odd">
<td>Data4 [7]</td>
<td>15</td>
<td>1</td>
<td>Este campo es obligatorio y contiene el sexto byte del quinto grupo del GUID (DAh del ejemplo).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10,2 tablas de particiones

Para garantizar la interoperabilidad de los volúmenes exFAT en un amplio conjunto de escenarios de uso, las implementaciones deben usar el tipo de partición 07H para el almacenamiento con particiones MBR y el GUID de partición {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} para el almacenamiento con particiones GPT.

## <a name="11-documentation-change-history"></a>11 historial de cambios de documentación

En la tabla 39 se describe el historial de versiones de, correcciones, adiciones, eliminaciones y aclaraciones de este documento.

<div id="table-39-documentation-change-history" />

**Tabla 39 historial de cambios de documentación**

<table>
<thead>
<tr class="header">
<th><strong>Date</strong></th>
<th><strong>Descripción del cambio</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Ene-2008</td>
<td><p>La primera versión de la especificación básica, que incluye:</p>
<blockquote>
<p>Sección 1, introducción</p>
<p>Sección 2,<br />
Estructura de volumen</p>
<p>Sección 3, regiones de arranque principales y de copia de seguridad</p>
<p>Sección 4, región de tabla de asignación de archivos</p>
<p>Sección 5, región de datos</p>
<p>Sección 6, estructura de directorios</p>
<p>Sección 7, definiciones de entradas de directorio</p>
<p>Sección 8, notas de implementación</p>
<p>Sección 9, límites del sistema de archivos</p>
<p>Sección 10, Apéndice</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-Jun-2008</td>
<td><p>Segunda versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Adición de la sección 11,<br />
Historial de cambios de documentación</p>
<p>Adición de las entradas de directorio de asignación de proveedor y de extensión de proveedor en las secciones 7,8 y 7,9</p>
<p>Adición de la tabla de casos de uso recomendado en las secciones 7.2.5 y 7.2.5.1</p>
<p>Adición de los campos UtcOffset en la sección 7,4 y adición del acrónimo UTC en la sección 1,3</p>
<p>Corrección del tamaño del campo CustomDefined en la tabla 19</p>
<p>Corrección del intervalo válido de valores de NameLength en la sección 7.6.3</p>
<p>Corrección y aclaración de los campos timestamp y 10msIncrement de la sección 7,4</p>
<p>Aclaración de la estructura de los parámetros null en la sección 3,3</p>
<p>Aclaración del significado de los valores del campo NoFatChain de la sección 6.3.4.2</p>
<p>Aclaración del significado de los valores del campo DATALENGTH en la sección 6.2.3</p>
<p>Aclaración del campo VolumeDirty de la sección 3.1.13.2 y orden de escritura recomendado en la sección 8,1</p>
<p>Aclaración del campo MediaFailure de la sección 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-Oct-2008</td>
<td><p>Tercera versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Incorporación de las explicaciones de los campos, y debe y puede hacerlo.</p>
<p>Adición de la definición de UTC en la sección 1,3 de la tabla 2</p>
<p>Se han modificado las secciones 1,5 para garantizar la alineación con el documento de especificación TexFAT.</p>
<p>Se ha aclarado la restricción de que solo Microsoft puede definir el diseño de las entradas de directorio en la sección 6,2</p>
<p>Se ha agregado una aclaración de que el campo FirstCluster debe ser cero si el valor de DATALENGTH es cero y NoFatChain está establecido en la sección 6.3.5 y en la sección 6.4.3</p>
<p>Requisitos clarificados para entradas de directorio de archivos válidas en la sección 7,4</p>
<p>Se agregó el requisito de nombres de archivo y directorio únicos a la sección 7,7</p>
<p>Se ha agregado la nota de implementación para ASCII al final de la sección 7.7.3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Ene-2009</td>
<td><p>Cuarta versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Se han quitado las referencias a Windows CE entradas de Access Control</p>
<p>Se ha agregado una aclaración a la sección 7.2.5.1 para requerir explícitamente una tabla completa de casos</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-Sep-2009</td>
<td><p>Quinta versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Cambios de formato del documento para permitir una mejor conversión de PDF</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24 de febrero de 2010</td>
<td><p>Sexta versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Se ha modificado la instrucción incorrecta: "el campo FirstCluster debe ser cero si el valor de DATALENGTH es cero y NoFatChain está establecido en" en la sección 6.3.5 y la sección 6.4.3 en "si el bit NoFatChain es 1, FirstCluster debe apuntar a un clúster válido en el montón del clúster" para aclarar que debe haber una asignación válida si se establece el bit NoFatChain.</p>
<p>Added "si el bit NoFatChain es 1, DATALENGTH no debe ser cero. Si el campo FirstCluster es cero, DATALENGTH también debe ser cero "a la sección 6.3.6 y la sección 6.4.4 para aclarar que debe haber una asignación válida si se establece el bit NoFatChain.</p>
<p>Aviso de copyright actualizado a 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26 de agosto de 2019</td>
<td><p>Séptima versión de la especificación básica, que incluye los cambios siguientes:</p>
<blockquote>
<p>Se han actualizado los términos legales correspondientes a la especificación, incluidos:</p>
<p>Eliminación de aviso confidencial de Microsoft</p>
<p>Sección del contrato de licencia de la documentación técnica de Microsoft Corporation</p>
<p>Aviso de copyright actualizado a 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
