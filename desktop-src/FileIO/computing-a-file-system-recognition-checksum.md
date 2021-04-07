---
description: La estructura de la \_ estructura de reconocimiento del sistema de archivos \_ \_ , definida internamente por Windows y utilizada por el reconocimiento del sistema de archivos (FRS), contiene un valor de suma de comprobación que debe calcularse correctamente para que FRS funcione correctamente con un sistema de archivos especificado no reconocido.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcular una suma de comprobación del reconocimiento del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003148"
---
# <a name="computing-a-file-system-recognition-checksum"></a><span data-ttu-id="95e1b-103">Calcular una suma de comprobación del reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="95e1b-103">Computing a File System Recognition Checksum</span></span>

<span data-ttu-id="95e1b-104">La estructura de la [**\_ \_ \_ estructura de reconocimiento del sistema de archivos**](file-system-recognition-structure.md) , definida internamente por Windows y utilizada por el [reconocimiento del sistema de archivos](file-system-recognition.md) (FRS), contiene un valor de suma de comprobación que debe calcularse correctamente para que FRS funcione correctamente con un sistema de archivos especificado no reconocido.</span><span class="sxs-lookup"><span data-stu-id="95e1b-104">The [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) structure, defined internally by Windows and used by [file system recognition](file-system-recognition.md) (FRS), contains a checksum value that must be properly computed for FRS to work properly with a specified unrecognized file system.</span></span> <span data-ttu-id="95e1b-105">En el ejemplo siguiente se realiza este cálculo.</span><span class="sxs-lookup"><span data-stu-id="95e1b-105">The following example accomplishes this computation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95e1b-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95e1b-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95e1b-107">Reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="95e1b-107">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="95e1b-108">**\_estructura de \_ reconocimiento del sistema de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="95e1b-108">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> </dl>

 

 



