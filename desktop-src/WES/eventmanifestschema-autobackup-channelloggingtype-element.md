---
title: AutoBackup (ChannelLoggingType) (elemento)
description: Determina si se debe crear un nuevo archivo de registro cuando el archivo de registro actual alcanza su tamaño máximo.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- elemento AutoBackup EventLog
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535463"
---
# <a name="autobackup-channelloggingtype-element"></a><span data-ttu-id="92b75-104">AutoBackup (ChannelLoggingType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="92b75-104">autoBackup (ChannelLoggingType) Element</span></span>

<span data-ttu-id="92b75-105">Determina si se debe crear un nuevo archivo de registro cuando el archivo de registro actual alcanza su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="92b75-105">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span>

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

<span data-ttu-id="92b75-106">El elemento **AutoBackup** se define mediante el tipo complejo [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="92b75-106">The **autoBackup** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b75-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b75-107">Requirements</span></span>



| <span data-ttu-id="92b75-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b75-108">Requirement</span></span> | <span data-ttu-id="92b75-109">Value</span><span class="sxs-lookup"><span data-stu-id="92b75-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92b75-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92b75-110">Minimum supported client</span></span><br/> | <span data-ttu-id="92b75-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92b75-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92b75-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92b75-112">Minimum supported server</span></span><br/> | <span data-ttu-id="92b75-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92b75-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92b75-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="92b75-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="92b75-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="92b75-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="92b75-116">**registro (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="92b75-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





