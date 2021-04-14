---
description: Contiene una matriz de blobs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Estructura de BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276699"
---
# <a name="blob_table-structure"></a><span data-ttu-id="1cc6b-103">\_Estructura de tabla BLOB</span><span class="sxs-lookup"><span data-stu-id="1cc6b-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="1cc6b-104">La estructura de la **\_ tabla BLOB** contiene una matriz de blobs.</span><span class="sxs-lookup"><span data-stu-id="1cc6b-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc6b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc6b-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="1cc6b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1cc6b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1cc6b-107">**dwNumBlobs**</span><span class="sxs-lookup"><span data-stu-id="1cc6b-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="1cc6b-108">Indicador que siguen muchos BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1cc6b-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="1cc6b-109">**hBlobs**</span><span class="sxs-lookup"><span data-stu-id="1cc6b-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="1cc6b-110">Identificador de la matriz de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1cc6b-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cc6b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc6b-111">Requirements</span></span>



| <span data-ttu-id="1cc6b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc6b-112">Requirement</span></span> | <span data-ttu-id="1cc6b-113">Value</span><span class="sxs-lookup"><span data-stu-id="1cc6b-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc6b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc6b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc6b-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1cc6b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1cc6b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cc6b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc6b-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cc6b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1cc6b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc6b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc6b-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc6b-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




