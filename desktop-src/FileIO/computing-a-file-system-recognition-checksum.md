---
description: La estructura FILE SYSTEM RECOGNITION STRUCTURE, definida internamente por Windows y utilizada por el reconocimiento del sistema de archivos \_ \_ (FRS), contiene un valor de suma de comprobación que se debe calcular correctamente para que FRS funcione correctamente con un sistema de archivos no reconocido \_ especificado.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcular una suma de comprobación de reconocimiento del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce146fda589668d39f1f7ff4158384986fb719f2bbbee6ce0584ad9f1e540b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329185"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Calcular una suma de comprobación de reconocimiento del sistema de archivos

La estructura [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE,**](file-system-recognition-structure.md) definida internamente por Windows y utilizada por el reconocimiento del sistema de archivos (FRS), contiene un valor de suma de comprobación que se debe calcular correctamente para que FRS funcione correctamente con un sistema de archivos no reconocido especificado. [](file-system-recognition.md) En el ejemplo siguiente se realiza este cálculo.


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reconocimiento del sistema de archivos](file-system-recognition.md)
</dt> <dt>

[**ESTRUCTURA DE \_ RECONOCIMIENTO DEL SISTEMA DE \_ \_ ARCHIVOS**](file-system-recognition-structure.md)
</dt> </dl>

 

 



