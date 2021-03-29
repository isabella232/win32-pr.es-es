---
description: Obtiene el uso actual del disco del usuario como una cadena de texto.
title: Propiedad DIDiskQuotaUser. QuotaUsedText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984263"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="53695-103">Propiedad DIDiskQuotaUser. QuotaUsedText</span><span class="sxs-lookup"><span data-stu-id="53695-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="53695-104">Obtiene el uso actual del disco del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="53695-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="53695-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53695-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53695-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53695-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="53695-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53695-107">Property value</span></span>

<span data-ttu-id="53695-108">Valor de cadena que se establece en la cantidad de espacio en disco que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="53695-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="53695-109">Si está habilitada la compresión de archivos NTFS, esta propiedad refleja la cantidad de espacio en disco que los datos necesitarían en un estado sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="53695-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="53695-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53695-110">Requirements</span></span>



| <span data-ttu-id="53695-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="53695-111">Requirement</span></span> | <span data-ttu-id="53695-112">Value</span><span class="sxs-lookup"><span data-stu-id="53695-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53695-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53695-113">Minimum supported client</span></span><br/> | <span data-ttu-id="53695-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53695-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53695-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53695-115">Minimum supported server</span></span><br/> | <span data-ttu-id="53695-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53695-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="53695-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53695-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53695-118"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="53695-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53695-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="53695-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53695-120">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="53695-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="53695-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="53695-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="53695-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="53695-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="53695-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="53695-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




