---
description: Representa un atributo de nombre de archivo. Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se escribe.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Estructura de FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080093"
---
# <a name="file_name-structure"></a><span data-ttu-id="38945-104">Estructura de nombre de archivo \_</span><span class="sxs-lookup"><span data-stu-id="38945-104">FILE\_NAME structure</span></span>

<span data-ttu-id="38945-105">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="38945-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="38945-106">Representa un atributo de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="38945-106">Represents a file name attribute.</span></span> <span data-ttu-id="38945-107">Un archivo tiene un atributo de nombre de archivo para cada directorio en el que se escribe.</span><span class="sxs-lookup"><span data-stu-id="38945-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="38945-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38945-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="38945-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="38945-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="38945-110">**ParentDirectory**</span><span class="sxs-lookup"><span data-stu-id="38945-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="38945-111">Referencia de archivo al directorio que indexa este nombre.</span><span class="sxs-lookup"><span data-stu-id="38945-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="38945-112">Consulte [**\_ \_ referencia de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="38945-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="38945-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="38945-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="38945-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="38945-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="38945-115">**FileNameLength**</span><span class="sxs-lookup"><span data-stu-id="38945-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="38945-116">La longitud del nombre de archivo, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="38945-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="38945-117">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="38945-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="38945-118">Marcas de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="38945-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="38945-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Archivo \_ de NOMBRE \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="38945-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="38945-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Archivo \_ de NAME \_ dos** (0x02)</span><span class="sxs-lookup"><span data-stu-id="38945-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="38945-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="38945-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="38945-122">Primer carácter del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="38945-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38945-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38945-123">Remarks</span></span>

<span data-ttu-id="38945-124">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="38945-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="38945-125">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="38945-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="38945-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="38945-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38945-127">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="38945-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
