---
description: Obtiene un valor booleano que indica si el archivo de cuota para el volumen se está recompilando actualmente.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propiedad DiskQuotaControl. QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984411"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="0f198-103">Propiedad DiskQuotaControl. QuotaFileRebuilding</span><span class="sxs-lookup"><span data-stu-id="0f198-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="0f198-104">Obtiene un valor booleano que indica si el archivo de cuota para el volumen se está recompilando actualmente.</span><span class="sxs-lookup"><span data-stu-id="0f198-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="0f198-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f198-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f198-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f198-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="0f198-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0f198-107">Property value</span></span>

<span data-ttu-id="0f198-108">Esta propiedad se establece en **true** si se vuelve a generar el archivo de cuota o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0f198-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f198-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f198-109">Remarks</span></span>

<span data-ttu-id="0f198-110">El archivo de cuota se vuelve a generar automáticamente cuando las cuotas están habilitadas en el sistema o cuando una o más entradas de usuario se marcan para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="0f198-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f198-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f198-111">Requirements</span></span>



| <span data-ttu-id="0f198-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f198-112">Requirement</span></span> | <span data-ttu-id="0f198-113">Value</span><span class="sxs-lookup"><span data-stu-id="0f198-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f198-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f198-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0f198-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0f198-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f198-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f198-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0f198-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f198-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0f198-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f198-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f198-119"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0f198-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f198-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f198-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f198-121">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="0f198-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




