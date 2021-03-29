---
description: Representa el tipo de ruta de acceso que se usa como argumento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumeración PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538367"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="f35b6-103">Enumeración de tipo de ruta de acceso \_</span><span class="sxs-lookup"><span data-stu-id="f35b6-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="f35b6-104">Representa el tipo de ruta de acceso que se usa como argumento.</span><span class="sxs-lookup"><span data-stu-id="f35b6-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f35b6-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f35b6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f35b6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f35b6-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**Ruta de acceso de DOS \_**</span><span class="sxs-lookup"><span data-stu-id="f35b6-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="f35b6-108">Ruta de acceso estándar.</span><span class="sxs-lookup"><span data-stu-id="f35b6-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="f35b6-109"><span id="NT_PATH"></span><span id="nt_path"></span>**\_ruta de acceso NT**</span><span class="sxs-lookup"><span data-stu-id="f35b6-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="f35b6-110">Ruta de acceso interna.</span><span class="sxs-lookup"><span data-stu-id="f35b6-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f35b6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f35b6-111">Requirements</span></span>



| <span data-ttu-id="f35b6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f35b6-112">Requirement</span></span> | <span data-ttu-id="f35b6-113">Value</span><span class="sxs-lookup"><span data-stu-id="f35b6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f35b6-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f35b6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f35b6-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f35b6-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f35b6-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f35b6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f35b6-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f35b6-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f35b6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f35b6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35b6-119">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="f35b6-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="f35b6-120">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="f35b6-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




