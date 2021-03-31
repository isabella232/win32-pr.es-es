---
description: Representa el encabezado de multisector.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Estructura de MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807063"
---
# <a name="multi_sector_header-structure"></a>Estructura de encabezado de varios \_ sectores \_

\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa el encabezado de multisector.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Signature**
</dt> <dd>

Signatura. Este valor es una comodidad para el usuario.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

Desplazamiento de la matriz de secuencias de actualización, desde el principio de esta estructura. La matriz de secuencias de actualización debe finalizar antes del último valor USHORT en el primer sector.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Tamaño de la matriz de secuencias de actualización, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

El encabezado multisector y la matriz de la secuencia de actualización proporcionan la detección de las transferencias de varios sectores incompletas para los dispositivos que tienen un tamaño de sector físico mayor o igual que el intervalo del número de secuencia (512) o que no transfieren los sectores fuera de orden. Si existe un dispositivo que tiene un tamaño de sector menor que el intervalo del número de secuencia y, a veces, transfiere sectores de forma desordenada, la matriz de secuencias de actualización no proporcionará una detección absoluta de las transferencias incompletas. El intervalo del número de secuencia se establece en un número lo suficientemente pequeño para proporcionar protección absoluta a todos los discos duros conocidos. No se establece un valor menor o es posible que haya un tiempo de ejecución excesivo o una sobrecarga de espacio.

La matriz de secuencias de actualización consta de una matriz de *n* valores **USHORT** , donde *n* es el tamaño de la estructura que se está protegiendo dividido por el intervalo del número de secuencia. La primera palabra contiene el número de secuencia de actualización, que es un contador cíclico del número de veces que la estructura contenedora se ha escrito en el disco. A continuación se muestran los valores de **USHORT** *guardados que el número* de secuencia de actualización sobrescribió la última vez que la estructura contenedora se escribió en el disco.

Cada vez que la estructura protegida está a punto de escribirse en el disco, la última palabra de cada intervalo del número de secuencia se guarda en su posición respectiva en la matriz del número de secuencia y, a continuación, se sobrescribe con el siguiente número de secuencia de actualización. Después de la escritura, o cada vez que se lee la estructura, la palabra guardada de la matriz del número de secuencia se restaura a su posición real en la estructura. Antes de restaurar las palabras guardadas en las lecturas, todos los números de secuencia al final de cada intervalo se comparan con el número de secuencia real al principio de la matriz. Si alguna de estas comparaciones no es igual, se ha detectado una transferencia multisector con errores.

El tamaño de la matriz viene determinado por el tamaño de la estructura contenedora. La matriz de secuencias de actualización debe estar incluida al final del encabezado de la estructura que protege debido a su tamaño variable. El usuario debe asegurarse de que el espacio correcto está reservado para la estructura contenedora: (Size of Structure/512 + 1) \* sizeof (USHORT).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
