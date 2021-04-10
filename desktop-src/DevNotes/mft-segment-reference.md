---
description: Representa una dirección en la tabla de archivos maestros (MFT). La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia del segmento MFT era válida.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Estructura de MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152710"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="0c07a-104">Estructura de referencia de \_ segmento MFT \_</span><span class="sxs-lookup"><span data-stu-id="0c07a-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="0c07a-105">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="0c07a-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="0c07a-106">Representa una dirección en la tabla de archivos maestros (MFT).</span><span class="sxs-lookup"><span data-stu-id="0c07a-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="0c07a-107">La dirección se etiqueta con un número de secuencia reutilizado circularmente que se establece en el momento en que la referencia del segmento MFT era válida.</span><span class="sxs-lookup"><span data-stu-id="0c07a-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c07a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c07a-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="0c07a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c07a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c07a-110">**SegmentNumberLowPart**</span><span class="sxs-lookup"><span data-stu-id="0c07a-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="0c07a-111">Parte baja del número de segmento.</span><span class="sxs-lookup"><span data-stu-id="0c07a-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="0c07a-112">**SegmentNumberHighPart**</span><span class="sxs-lookup"><span data-stu-id="0c07a-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="0c07a-113">Parte alta del número de segmento.</span><span class="sxs-lookup"><span data-stu-id="0c07a-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="0c07a-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0c07a-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0c07a-115">Número de secuencia distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0c07a-115">The nonzero sequence number.</span></span> <span data-ttu-id="0c07a-116">El valor 0 está reservado.</span><span class="sxs-lookup"><span data-stu-id="0c07a-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c07a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c07a-117">Remarks</span></span>

<span data-ttu-id="0c07a-118">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="0c07a-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="0c07a-119">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="0c07a-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="0c07a-120">El tipo de datos de **\_ referencia de archivo** se define como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c07a-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="0c07a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c07a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c07a-122">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="0c07a-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
