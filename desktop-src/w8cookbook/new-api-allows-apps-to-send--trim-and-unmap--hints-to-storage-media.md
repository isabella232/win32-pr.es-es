---
title: La nueva API permite que las aplicaciones envíen sugerencias "TRIM y Unmap" a los medios de almacenamiento.
description: La nueva API permite que las aplicaciones envíen \ 0034; TRIM y Unmap \ 0034; sugerencias a medios de almacenamiento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247652"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>La nueva API permite que las aplicaciones envíen sugerencias "TRIM y Unmap" a los medios de almacenamiento.

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

Las sugerencias TRIM notifican a la unidad que determinados sectores asignados anteriormente ya no son necesarios para la aplicación y se pueden purgar. Esto se usa normalmente cuando una aplicación realiza asignaciones de espacio grande a través de un archivo y, a continuación, administra las asignaciones al archivo (por ejemplo, archivos de disco duro virtual).

**¿Qué es TRIM?**

Las unidades de estado sólido (SSD) suelen ser dispositivos borrados por bloques basados en memoria flash. Esto significa que, cuando los datos se escriben en ssd, no se pueden escribir en exceso en su lugar y deben escribirse en otro lugar hasta que el bloque se pueda recopilar como elementos no utilizados. Dado que ssd no tiene ningún mecanismo interno para determinar que se quitan determinados bloques y se necesitan otros. La única vez que ssd puede marcar un sector "desnuciado" es cuando se sobresalta. En otros casos, como cuando se elimina un archivo, ssd conserva estos sectores porque la eliminación se realiza como una tabla de archivos maestros (MFT) solo cambia y no como una operación para todos los sectores del archivo. En Windows 7, presentamos una manera estándar de comunicarse con los DS sobre los sectores que ya no son necesarios. Este comando se define en la especificación [T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como el comando TRIM; NTFS envía el comando TRIM para algunas operaciones insertas normales, como "deletefile".

**Otros usos de TRIM en el mundo del almacenamiento**

Al igual que los SSD, las redes de área de almacenamiento (SAN) y la nueva característica Windows 8 las implementaciones de espacios de software consumen sugerencias de comando TRIM para administrar sus espacios en entornos con aprovisionamiento fino. Las SAN y los espacios de software asignan regiones de almacenamiento en tamaños mayores que los sectores o clústeres (desde 1 MB a 1 GB). Cuando reciben sugerencias TRIM para su tamaño de asignación (o mayor que el tamaño de asignación), san/SSD puede desasignar una región para liberar espacio para otros archivos. Normalmente pasan a través de todas las sugerencias TRIM al medio subyacente (SSD o HDD) para que puedan consumir el espacio libre según corresponda. Normalmente no mueven datos a regiones desasignadas, ni hacen un seguimiento de las áreas TRIM a regiones desasignadas (cuando la región está vacía).

Las SAN de aprovisionamiento fino usan las sugerencias TRIM que se les pasan para ayudar a reducir la superficie de almacenamiento físico general, lo que reduce el costo. La [especificación SCSI T10](https://www.t10.org) define el comando "Unmap" (similar al comando TRIM); aquí el comando es aplicable a todos los tipos de almacenamiento, incluidos los DS, los DS y otros. El comando UnMap ayuda a quitar bloques físicos de la asignación de SAN.

## <a name="how-to-use-the-new-api"></a>Uso de la nueva API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



El archivo TRIM se pasa a través del búfer si es posible o de forma asincrónica (sin búfer) al comando TRIM del DSM de IOCTL del dispositivo. Esto se asigna al comando TRIM para dispositivos ATA y al comando UnMap para dispositivos SCSI. El código TRIM de archivo envía las regiones una a una según lo especificado por las extensiones anteriores.

Trim de archivo no espera las devoluciones del dispositivo, porque los comandos TRIM y Unmap se definen como sugerencias para los medios de almacenamiento subyacentes y no se esperan códigos de retorno.

**Flujo de trabajo de un extremo a otro:**

1.  Recorte del archivo de llamada
    1.  Trim de archivo examina las entradas en busca de errores
    2.  El archivo TRIM divide las extensiones en regiones LCN
    3.  Trim de archivo se redondea hacia arriba y hacia abajo para las regiones mal alineadas que se pasan a TRIM
    4.  Trim de archivo purga las entradas de la memoria caché relacionadas con las áreas TRIM
    5.  File TRIM pasa IOCTL \_ DSM (Trim) por región
2.  Errores o devoluciones de TRIM de archivo
    1.  La comprobación de errores se realiza en la validez de la entrada
    2.  Si solo algunas de las extensiones son válidas, se devuelve un error para la llamada API completa.

**Casos de uso**

**Disco duro virtual (VHD) de consumidor montado en un DISCO SSD:**

El disco duro virtual se monta inicialmente en medios "limpios" sin usar. A medida que se usa el disco duro virtual, el VHD consume partes del medio de almacenamiento para los archivos, etc. Cuando elimina archivos en el medio de almacenamiento, estos archivos no se quitan de SSD, ya que el VHD completo se almacena como un archivo en ssd. El entorno de Hyper-V llama a File TRIM para todas las regiones que se eliminan cuando se produce delete-file en el entorno de VHD. Las \_ TDM de archivo se traducen a SSD para que se pueda optimizar el rendimiento de SSD.

**VHD de consumidor montado en una SAN de aprovisionamiento fino:**

El disco duro virtual se monta inicialmente en una losa mínima de un entorno de aprovisionamiento fino. A medida que los archivos se almacenan en el disco duro virtual, la superficie de almacenamiento del disco duro virtual crece en múltiplo de losas. Cuando se quitan archivos en el disco duro virtual, Hyper-V llama a \_ File TRIM a la SAN de aprovisionamiento fino subyacente. Si las TDM son mayores que la granularidad de SLAB, la SAN ahora puede quitar un SLAB y, por tanto, reducir la superficie del VHD en esa SAN.

Si el disco duro virtual se encuentra en un servidor basado en Windows 8, el optimizador de Storage también enviará TDM para reducir la superficie de losa del disco duro virtual desde dentro del VHD montado.

## <a name="tests"></a>Pruebas

No hay NINGUNA API comparable en versiones anteriores del sistema operativo. No debería haber ningún impacto en el rendimiento de la propia API real, aunque los medios de almacenamiento (si se implementan correctamente) pueden mostrar un mejor rendimiento de escritura. La API debe usarse con mucho cuidado; solo se deben pasar las extensiones que ya no sean necesarias, ya que esas extensiones se quitarán permanentemente de los medios de almacenamiento.

## <a name="resources"></a>Recursos

-   [Especificación T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Especificación SCSI T10](https://www.t10.org/)

 

 




