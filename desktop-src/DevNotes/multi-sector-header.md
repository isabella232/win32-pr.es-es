---
description: Representa el encabezado multisector.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER estructura
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
ms.openlocfilehash: 9e34e23d3d2bf2ecfbc1c668e02c177e4d1516c73acabccc88aa7190ec33e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667222"
---
# <a name="multi_sector_header-structure"></a>Estructura \_ DE ENCABEZADO MULTI SECTOR \_

\[Esta estructura solo es válida para la versión 3 de volúmenes NTFS; se puede modificar en versiones futuras.\]

Representa el encabezado multisector.

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

Desplazamiento a la matriz de secuencia de actualización, desde el principio de esta estructura. La matriz de secuencias de actualización debe finalizar antes del último valor USHORT del primer sector.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Tamaño de la matriz de secuencia de actualización, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.

Esta definición de estructura solo es válida para la versión principal 3 y la versión secundaria 0 o 1, como notifica [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

El encabezado multisector y la matriz de secuencias de actualización proporcionan la detección de transferencias multisector incompletas para dispositivos que tienen un tamaño de sector físico mayor o igual que el paso del número de secuencia (512) o que no transfieren sectores desfasados. Si existe un dispositivo que tiene un tamaño de sector menor que el paso del número de secuencia y, a veces, transfiere sectores fuera de orden, la matriz de secuencias de actualización no proporcionará la detección absoluta de transferencias incompletas. El paso del número de secuencia se establece en un número lo suficientemente pequeño como para proporcionar una protección absoluta para todos los discos duros conocidos. No se establece ningún valor más pequeño o puede haber un tiempo de ejecución excesivo o sobrecarga de espacio.

La matriz de secuencia de actualización consta de una matriz de *n* valores **USHORT,** donde *n* es el tamaño de la estructura que se protege dividida por el número de secuencia stride. La primera palabra contiene el número de secuencia de actualización, que es un contador cíclico del número de veces que la estructura que contiene se ha escrito en el disco. A continuación se *encuentran los n* valores **USHORT** guardados que se sobrescribiron por el número de secuencia de actualización la última vez que se escribió la estructura que contiene en el disco.

Cada vez que la estructura protegida está a punto de escribirse en el disco, la última palabra de cada paso de número de secuencia se guarda en su posición respectiva en la matriz de números de secuencia y, a continuación, se sobrescribe con el siguiente número de secuencia de actualización. Después de la escritura, o cada vez que se lee la estructura, la palabra guardada de la matriz de números de secuencia se restaura a su posición real en la estructura . Antes de restaurar las palabras guardadas en las lecturas, todos los números de secuencia al final de cada paso se comparan con el número de secuencia real al principio de la matriz. Si alguna de estas comparaciones no es igual, se ha detectado un error en la transferencia multisector.

El tamaño de la matriz viene determinado por el tamaño de la estructura que lo contiene. La matriz de secuencias de actualización debe incluirse al final del encabezado de la estructura que protege debido a su tamaño variable. El usuario debe asegurarse de que el espacio correcto está reservado para la estructura que lo contiene: (tamaño de structure /512 + 1) \* sizeof(USHORT).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tabla de archivos maestros](master-file-table.md)
</dt> </dl>

 

 
