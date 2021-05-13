---
description: Obtiene el nombre del contenedor de cuentas del usuario.
title: Propiedad DIDiskQuotaUser.AccountContainerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843356"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="98eaa-103">Propiedad DIDiskQuotaUser.AccountContainerName</span><span class="sxs-lookup"><span data-stu-id="98eaa-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="98eaa-104">Obtiene el nombre del contenedor de cuentas del usuario.</span><span class="sxs-lookup"><span data-stu-id="98eaa-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="98eaa-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="98eaa-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="98eaa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98eaa-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="98eaa-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="98eaa-107">Property value</span></span>

<span data-ttu-id="98eaa-108">Valor de cadena que se establece en el nombre del contenedor de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="98eaa-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="98eaa-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98eaa-109">Remarks</span></span>

<span data-ttu-id="98eaa-110">Para las cuentas sin información de servicios de directorio, esta propiedad contiene el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="98eaa-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="98eaa-111">Para las cuentas con información de servicios de directorio, esta propiedad contiene un nombre canónico con el nombre del objeto de terminación quitado.</span><span class="sxs-lookup"><span data-stu-id="98eaa-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="98eaa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98eaa-112">Requirements</span></span>



| <span data-ttu-id="98eaa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98eaa-113">Requirement</span></span> | <span data-ttu-id="98eaa-114">Value</span><span class="sxs-lookup"><span data-stu-id="98eaa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98eaa-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98eaa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="98eaa-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98eaa-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98eaa-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98eaa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="98eaa-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98eaa-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="98eaa-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98eaa-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98eaa-120"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="98eaa-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98eaa-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98eaa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98eaa-122">**DIDiskQuotaUser (objeto)**</span><span class="sxs-lookup"><span data-stu-id="98eaa-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




