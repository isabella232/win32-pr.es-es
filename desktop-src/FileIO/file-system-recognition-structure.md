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
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="53df6-103">Estructura de la \_ estructura de reconocimiento del sistema de archivos \_ \_</span><span class="sxs-lookup"><span data-stu-id="53df6-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="53df6-104">Contiene la información de reconocimiento del sistema de archivos en disco almacenada en el sector de arranque del volumen (el sector del disco lógico cero).</span><span class="sxs-lookup"><span data-stu-id="53df6-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="53df6-105">Se trata de una estructura de datos definida internamente que no está disponible en un encabezado público y que se proporciona aquí para los desarrolladores del sistema de archivos que desean aprovechar el reconocimiento del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="53df6-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="53df6-106">Para obtener más información, consulte [reconocimiento del sistema de archivos](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="53df6-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="53df6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53df6-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="53df6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="53df6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="53df6-109">**JMP**</span><span class="sxs-lookup"><span data-stu-id="53df6-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-110">La instrucción JMP.</span><span class="sxs-lookup"><span data-stu-id="53df6-110">The JMP instruction.</span></span> <span data-ttu-id="53df6-111">Este miembro de datos no se incluye en el valor contenido en el miembro de datos de la **suma de comprobación** .</span><span class="sxs-lookup"><span data-stu-id="53df6-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="53df6-112">**FsName**</span><span class="sxs-lookup"><span data-stu-id="53df6-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-113">Nombre del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="53df6-113">The file system name.</span></span> <span data-ttu-id="53df6-114">Se trata de una secuencia de 8 caracteres ASCII que representa el nombre legible no traducible del sistema de archivos con el que se da formato al volumen.</span><span class="sxs-lookup"><span data-stu-id="53df6-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="53df6-115">Esta cadena está en el mismo lugar que el nombre del sistema de archivos OEM en un disco con una estructura normal de bloque de parámetros del BIOS (BPB).</span><span class="sxs-lookup"><span data-stu-id="53df6-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="53df6-116">**MustBeZero**</span><span class="sxs-lookup"><span data-stu-id="53df6-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-117">Espacio reservado que contiene todos los ceros.</span><span class="sxs-lookup"><span data-stu-id="53df6-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="53df6-118">Este miembro de datos se superpone a lo que normalmente son los siguientes miembros de datos en un BPB:</span><span class="sxs-lookup"><span data-stu-id="53df6-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="53df6-119">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="53df6-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="53df6-120">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="53df6-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="53df6-121">**ReservedSectorCount**</span><span class="sxs-lookup"><span data-stu-id="53df6-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="53df6-122">Dado que estos miembros de datos se establecen en cero, esto debe ser suficiente para que los sistemas operativos anteriores puedan concluir que no es un BPB válido y, por lo tanto, reconocen el volumen.</span><span class="sxs-lookup"><span data-stu-id="53df6-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="53df6-123">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="53df6-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-124">Identificador de estructura.</span><span class="sxs-lookup"><span data-stu-id="53df6-124">A structure identifier.</span></span> <span data-ttu-id="53df6-125">Debe contener el valor 0x53525346 organizado en orden de bytes Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="53df6-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="53df6-126">En este punto de la estructura, los datos se alinean con 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="53df6-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53df6-127">**Duración**</span><span class="sxs-lookup"><span data-stu-id="53df6-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-128">Número de bytes de esta estructura, desde el principio hasta el final, incluido el miembro de datos **JMP** .</span><span class="sxs-lookup"><span data-stu-id="53df6-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="53df6-129">**MD5**</span><span class="sxs-lookup"><span data-stu-id="53df6-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="53df6-130">Suma de comprobación de dos bytes calculada sobre los bytes que comienzan en el miembro de datos **FsName** y terminando en el último byte de esta estructura, sin incluir los miembros de datos **JMP** y **checksum** .</span><span class="sxs-lookup"><span data-stu-id="53df6-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53df6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53df6-131">Requirements</span></span>



| <span data-ttu-id="53df6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="53df6-132">Requirement</span></span> | <span data-ttu-id="53df6-133">Value</span><span class="sxs-lookup"><span data-stu-id="53df6-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="53df6-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53df6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53df6-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="53df6-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="53df6-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53df6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53df6-137">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="53df6-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53df6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="53df6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53df6-139">Calcular una suma de comprobación del reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="53df6-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="53df6-140">Reconocimiento del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="53df6-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="53df6-141">**\_información de \_ reconocimiento del sistema de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="53df6-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="53df6-142">**\_ \_ \_ reconocimiento del sistema de archivos de consulta FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="53df6-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

