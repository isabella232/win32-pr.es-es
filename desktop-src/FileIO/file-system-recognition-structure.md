---
description: 'Contiene la información de reconocimiento del sistema de archivos en disco almacenada en el sector de arranque volúmenes (disco lógico: cero).'
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Estructura de FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082411"
---
# <a name="file_system_recognition_structure-structure"></a>Estructura de la \_ estructura de reconocimiento del sistema de archivos \_ \_

Contiene la información de reconocimiento del sistema de archivos en disco almacenada en el sector de arranque del volumen (el sector del disco lógico cero).

Se trata de una estructura de datos definida internamente que no está disponible en un encabezado público y que se proporciona aquí para los desarrolladores del sistema de archivos que desean aprovechar el reconocimiento del sistema de archivos. Para obtener más información, consulte [reconocimiento del sistema de archivos](file-system-recognition.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**JMP**
</dt> <dd>

La instrucción JMP. Este miembro de datos no se incluye en el valor contenido en el miembro de datos de la **suma de comprobación** .

</dd> <dt>

**FsName**
</dt> <dd>

Nombre del sistema de archivos. Se trata de una secuencia de 8 caracteres ASCII que representa el nombre legible no traducible del sistema de archivos con el que se da formato al volumen.

Esta cadena está en el mismo lugar que el nombre del sistema de archivos OEM en un disco con una estructura normal de bloque de parámetros del BIOS (BPB).

</dd> <dt>

**MustBeZero**
</dt> <dd>

Espacio reservado que contiene todos los ceros.

Este miembro de datos se superpone a lo que normalmente son los siguientes miembros de datos en un BPB:

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

Dado que estos miembros de datos se establecen en cero, esto debe ser suficiente para que los sistemas operativos anteriores puedan concluir que no es un BPB válido y, por lo tanto, reconocen el volumen.

</dd> <dt>

**Identificador**
</dt> <dd>

Identificador de estructura. Debe contener el valor 0x53525346 organizado en orden de bytes Little-Endian.

En este punto de la estructura, los datos se alinean con 16 bytes.

</dd> <dt>

**Duración**
</dt> <dd>

Número de bytes de esta estructura, desde el principio hasta el final, incluido el miembro de datos **JMP** .

</dd> <dt>

**MD5**
</dt> <dd>

Suma de comprobación de dos bytes calculada sobre los bytes que comienzan en el miembro de datos **FsName** y terminando en el último byte de esta estructura, sin incluir los miembros de datos **JMP** y **checksum** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calcular una suma de comprobación del reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Reconocimiento del sistema de archivos](file-system-recognition.md)
</dt> <dt>

[**\_información de \_ reconocimiento del sistema de archivos \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**\_ \_ \_ reconocimiento del sistema de archivos de consulta FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

