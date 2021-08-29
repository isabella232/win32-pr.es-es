---
description: Contiene la información de reconocimiento del sistema de archivos en disco almacenada en el sector de arranque de volúmenes (sector de disco lógico cero).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: FILE_SYSTEM_RECOGNITION_STRUCTURE estructura
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
ms.openlocfilehash: 5f18634e3f160347a841008ec24a22c9443e92c546d0637da791b5b4a9c81522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696245"
---
# <a name="file_system_recognition_structure-structure"></a>ESTRUCTURA DE \_ RECONOCIMIENTO DEL SISTEMA DE \_ \_ ARCHIVOS

Contiene la información de reconocimiento del sistema de archivos en disco almacenada en el sector de arranque del volumen (sector de disco lógico cero).

Se trata de una estructura de datos definida internamente que no está disponible en un encabezado público y se proporciona aquí para los desarrolladores de sistemas de archivos que desean aprovechar el reconocimiento del sistema de archivos. Para obtener más información, vea [Reconocimiento del sistema de archivos](file-system-recognition.md).

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

**Jmp**
</dt> <dd>

Instrucción JMP. Este miembro de datos no se incluye en el valor contenido en el miembro **de datos Checksum.**

</dd> <dt>

**FsName**
</dt> <dd>

Nombre del sistema de archivos. Se trata de una secuencia de 8 caracteres ASCII que representa el nombre legible no localizable del sistema de archivos con el que se da formato al volumen.

Esta cadena se encuentra en el mismo lugar que el nombre del sistema de archivos OEM en un disco con una estructura de bloque de parámetros BIOS (BPB) normal.

</dd> <dt>

**MustBeZero**
</dt> <dd>

Espacio reservado que contiene todos los ceros.

Este miembro de datos se superpone a lo que normalmente son los siguientes miembros de datos en un BPB:

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

Dado que estos miembros de datos están establecidos en cero, esto debería ser suficiente para hacer que los sos anteriores concluyese que no se trata de un BPB válido y, por tanto, reconocen el volumen.

</dd> <dt>

**Identificador**
</dt> <dd>

Identificador de estructura. Debe contener el valor 0x53525346 organizado en orden de bytes little-endian.

En este punto de la estructura, los datos se alinean con 16 bytes.

</dd> <dt>

**Duración**
</dt> <dd>

Número de bytes de esta estructura, desde el principio hasta el final, incluido el **miembro de datos Jmp.**

</dd> <dt>

**Checksum**
</dt> <dd>

Suma de comprobación de dos bytes calculada sobre los bytes que comienzan en el miembro de datos **FsName** y terminan en el último byte de esta estructura, excepto los miembros de datos **Jmp** y **Checksum.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Calcular una suma de comprobación de reconocimiento del sistema de archivos](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Reconocimiento del sistema de archivos](file-system-recognition.md)
</dt> <dt>

[**INFORMACIÓN DE \_ RECONOCIMIENTO DEL SISTEMA DE \_ \_ ARCHIVOS**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**RECONOCIMIENTO DEL SISTEMA \_ DE ARCHIVOS DE CONSULTA \_ \_ \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

