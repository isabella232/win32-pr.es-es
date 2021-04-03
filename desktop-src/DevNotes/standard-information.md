---
description: Contiene el atributo de información estándar. Este atributo está presente en cada registro de archivo base y debe ser residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Estructura de STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080085"
---
# <a name="standard_information-structure"></a><span data-ttu-id="42f82-104">\_Estructura de información estándar</span><span class="sxs-lookup"><span data-stu-id="42f82-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="42f82-105">\[Esta estructura solo es válida para la versión 3 de los volúmenes NTFS; se puede modificar en versiones futuras.\]</span><span class="sxs-lookup"><span data-stu-id="42f82-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="42f82-106">Contiene el atributo de información estándar.</span><span class="sxs-lookup"><span data-stu-id="42f82-106">Contains the standard information attribute.</span></span> <span data-ttu-id="42f82-107">Este atributo está presente en cada registro de archivo base y debe ser residente.</span><span class="sxs-lookup"><span data-stu-id="42f82-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f82-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42f82-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="42f82-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="42f82-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="42f82-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="42f82-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="42f82-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="42f82-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42f82-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="42f82-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="42f82-113">Identificador del propietario del archivo, del índice de seguridad.</span><span class="sxs-lookup"><span data-stu-id="42f82-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="42f82-114">**SecurityId**</span><span class="sxs-lookup"><span data-stu-id="42f82-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="42f82-115">El identificador de seguridad del archivo.</span><span class="sxs-lookup"><span data-stu-id="42f82-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42f82-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42f82-116">Remarks</span></span>

<span data-ttu-id="42f82-117">Tenga en cuenta que no hay ningún archivo de encabezado asociado para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="42f82-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="42f82-118">Esta definición de estructura solo es válida para la versión 3 principal y la secundaria 0 o 1, tal y como lo ha indicado el [**FSCTL \_ obtener \_ \_ \_ datos del volumen NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="42f82-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="42f82-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f82-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f82-120">Tabla de archivos maestros</span><span class="sxs-lookup"><span data-stu-id="42f82-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
