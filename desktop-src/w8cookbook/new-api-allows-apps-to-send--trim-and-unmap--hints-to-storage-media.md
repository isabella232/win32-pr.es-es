---
title: La nueva API permite que las aplicaciones envíen sugerencias "recortar y desasignar" a los medios de almacenamiento
description: La nueva API permite que las aplicaciones envíen \ 0034; TRIM y desasignar \ 0034; sugerencias para medios de almacenamiento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105695774"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>La nueva API permite que las aplicaciones envíen sugerencias "recortar y desasignar" a los medios de almacenamiento

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

Las sugerencias de recorte notifican a la unidad que ciertos sectores que anteriormente se asignaron ya no son necesarios para la aplicación y se pueden purgar. Normalmente se usa cuando una aplicación realiza asignaciones de espacio grande a través de un archivo y, a continuación, administra automáticamente las asignaciones en el archivo (por ejemplo, archivos de disco duro virtual).

**¿Qué es TRIM?**

Las unidades de estado sólido (SSD) suelen ser dispositivos con bloqueo en bloque basado en memoria Flash. Esto significa que cuando se escriben datos en la SSD, no se puede sobrescribir en su lugar y se deben escribir en otro lugar hasta que el bloque se pueda recolectar como elemento no utilizado. Dado que SSD no tiene ningún mecanismo interno para determinar que se han quitado determinados bloques y que se necesitan otros. La única vez que SSD puede marcar un sector como ' sucio ' es cuando está sobrescrito. En otros casos, como cuando se elimina un archivo, el SSD conserva estos sectores, ya que la eliminación se realiza solo como un cambio en la tabla de archivos maestros (MFT) y no como una operación para todos los sectores del archivo. En Windows 7, se presentó una forma estándar de comunicarse con SSD sobre sectores que no son necesarios. Este comando se define en la [especificación T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como el comando Trim. NTFS envía el comando TRIM para algunas operaciones en línea normales, como "DeleteFile".

**Otros usos de TRIM en el mundo de almacenamiento**

Como las SSD, las redes de área de almacenamiento (San) y las nuevas implementaciones de espacios de software de características de Windows 8 usan sugerencias de comando de recorte para administrar sus espacios en entornos con aprovisionamiento fino. Las San y los espacios de software asignan regiones de almacenamiento en tamaños que son mayores que los sectores o clústeres (desde 1 MB a 1 GB). Cuando reciben sugerencias de recorte para su tamaño de asignación (o mayor que el tamaño de asignación), la SAN o SSD puede anular la asignación de una región para liberar espacio para otros archivos. Normalmente pasan por todas las sugerencias de recorte al medio subyacente (SSD o HDD) para que puedan consumir el espacio liberado según corresponda. Normalmente no mueven los datos a las regiones de anulación de asignación, ni realizan un seguimiento de las áreas de recorte a regiones desasignadas (cuando la región está vacía).

Las redes San con aprovisionamiento fino usan las sugerencias de recorte que se les pasan para ayudar a reducir la superficie general de almacenamiento físico, lo que reduce el costo. La [especificación de SCSI de T10](https://www.t10.org) define el comando "desasignar" (similar al comando Trim); Aquí el comando es aplicable a todos los tipos de almacenamiento, incluidos HDD, SSD y otros. El comando desasignar ayuda a quitar los bloques físicos de la asignación de la SAN.

## <a name="how-to-use-the-new-api"></a>Cómo usar la nueva API


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



El recorte de archivos se pasa a través del búfer si es posible o de forma asincrónica (no almacenada en búfer) al recorte del comando DSM de IOCTL del dispositivo. Esto se asigna al comando de recorte para dispositivos ATA y al comando desasociar para dispositivos SCSI. El código de recorte de archivos envía las regiones una por una, tal y como se especifica en las extensiones anteriores.

El recorte de archivos no espera las devoluciones del dispositivo, ya que los comandos de recorte y desasignación se definen como sugerencias para los medios de almacenamiento subyacentes y los códigos de retorno no se esperan.

**Flujo de trabajo de un extremo a otro:**

1.  Recorte del archivo de llamadas
    1.  El recorte de archivos examina las entradas en busca de errores
    2.  El recorte de archivos divide las extensiones en regiones de LCN
    3.  El recorte de archivo se redondea hacia arriba y hacia abajo para las regiones no alineadas que se pasan a TRIM
    4.  El recorte de archivos purga las entradas de la memoria caché que están relacionadas con las áreas de recorte
    5.  El recorte de archivos supera IOCTL \_ DSM (Trim) por región
2.  Errores o devoluciones de recorte de archivos
    1.  La comprobación de errores se realiza en la validez de la entrada
    2.  Si solo algunas de las extensiones son válidas, se devuelve un error para la llamada de API completa

**Casos de uso**

**Disco duro virtual (VHD) de consumidor montado en una SSD:**

El disco duro virtual se monta inicialmente en un medio sin usar "Clean". A medida que se usa el disco duro virtual, el disco duro virtual consume partes de los medios de almacenamiento para los archivos, etc. Cuando elimina archivos en el medio de almacenamiento, estos archivos no se quitan de la SSD, ya que el disco duro virtual completo se almacena como un archivo en la SSD. El entorno de Hyper-V llama al recorte de archivos para todas las regiones que se eliminan cuando se produce delete-file en el entorno de VHD. Los \_ recortes de archivo se traducen a la SSD para que se pueda optimizar el rendimiento de SSD.

**VHD de consumidor montado en una SAN con aprovisionamiento fino:**

El disco duro virtual se monta inicialmente en una losa mínima de un entorno con aprovisionamiento fino. A medida que los archivos se almacenan en el disco duro virtual, la superficie de almacenamiento del disco duro virtual crece en múltiplos de bloques. Cuando se quitan archivos en el disco duro virtual, Hyper-V llama al recorte de archivos en \_ la red San de aprovisionamiento fino subyacente. Si los recortes son mayores que la granularidad de los bloques, la SAN puede quitar ahora una losa y, por tanto, reducir la superficie del VHD en esa SAN.

Si el disco duro virtual reside en un servidor basado en Windows 8, el optimizador de almacenamiento también enviará recortes para reducir la superficie de la losa del VHD desde el VHD montado.

## <a name="tests"></a>Pruebas

No hay ninguna API comparable en las versiones anteriores del sistema operativo. No debería haber ningún impacto en el rendimiento de la propia API real, aunque el medio de almacenamiento (si se implementa correctamente) puede mostrar un mejor rendimiento de escritura. La API debe usarse con sumo cuidado; solo se deben pasar las extensiones que ya no sean necesarias, ya que esas extensiones se quitarán permanentemente de los medios de almacenamiento.

## <a name="resources"></a>Recursos

-   [Especificación de T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Especificación de SCSI de T10](https://www.t10.org/)

 

 




