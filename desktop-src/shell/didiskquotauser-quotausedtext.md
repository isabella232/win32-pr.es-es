---
description: Obtiene el uso actual del disco del usuario como una cadena de texto.
title: Propiedad DIDiskQuotaUser.QuotaUsedText
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
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843216"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="2c748-103">Propiedad DIDiskQuotaUser.QuotaUsedText</span><span class="sxs-lookup"><span data-stu-id="2c748-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="2c748-104">Obtiene el uso actual del disco del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="2c748-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="2c748-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2c748-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c748-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c748-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="2c748-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c748-107">Property value</span></span>

<span data-ttu-id="2c748-108">Valor de cadena que se establece en la cantidad de espacio en disco actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="2c748-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="2c748-109">Si la compresión de archivos NTFS está habilitada, esta propiedad refleja la cantidad de espacio en disco que los datos requerirían en un estado sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2c748-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c748-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c748-110">Requirements</span></span>



| <span data-ttu-id="2c748-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c748-111">Requirement</span></span> | <span data-ttu-id="2c748-112">Value</span><span class="sxs-lookup"><span data-stu-id="2c748-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c748-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c748-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2c748-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c748-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c748-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c748-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2c748-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c748-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2c748-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c748-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c748-118"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2c748-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c748-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c748-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c748-120">**DIDiskQuotaUser (objeto)**</span><span class="sxs-lookup"><span data-stu-id="2c748-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="2c748-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="2c748-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="2c748-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="2c748-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="2c748-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="2c748-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




