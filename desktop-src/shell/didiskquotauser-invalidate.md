---
description: Borra la información de usuario almacenada en caché del objeto.
title: Método DIDiskQuotaUser.Invalidate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843276"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="98202-103">Método DIDiskQuotaUser.Invalidate</span><span class="sxs-lookup"><span data-stu-id="98202-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="98202-104">Borra la información de usuario almacenada en caché del objeto.</span><span class="sxs-lookup"><span data-stu-id="98202-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="98202-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98202-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="98202-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98202-106">Parameters</span></span>

<span data-ttu-id="98202-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="98202-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98202-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98202-108">Return value</span></span>

<span data-ttu-id="98202-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="98202-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98202-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98202-110">Remarks</span></span>

<span data-ttu-id="98202-111">Este método borra la información del usuario almacenada en la memoria caché del objeto.</span><span class="sxs-lookup"><span data-stu-id="98202-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="98202-112">La próxima vez que se realiza una solicitud de información relacionada con la cuota, el objeto recupera la información del volumen NTFS y actualiza la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="98202-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="98202-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98202-113">Requirements</span></span>



| <span data-ttu-id="98202-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98202-114">Requirement</span></span> | <span data-ttu-id="98202-115">Value</span><span class="sxs-lookup"><span data-stu-id="98202-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98202-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98202-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98202-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98202-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98202-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98202-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98202-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98202-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="98202-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98202-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98202-121"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="98202-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98202-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98202-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98202-123">**DIDiskQuotaUser (objeto)**</span><span class="sxs-lookup"><span data-stu-id="98202-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




