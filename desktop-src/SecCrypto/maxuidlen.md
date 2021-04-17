---
description: Constante numérica que especifica el número máximo de caracteres que utilizarán algunos de los proveedores de servicios criptográficos de Microsoft al obtener el identificador de usuario.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686872"
---
# <a name="maxuidlen"></a><span data-ttu-id="75646-103">MAXUIDLEN</span><span class="sxs-lookup"><span data-stu-id="75646-103">MAXUIDLEN</span></span>

<span data-ttu-id="75646-104">MAXUIDLEN es una constante numérica que especifica el número máximo de caracteres que utilizarán algunos de los proveedores de servicios criptográficos de Microsoft al obtener el ID. de usuario. MAXUIDLEN se define en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="75646-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="75646-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="75646-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="75646-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="75646-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="75646-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="75646-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="75646-108">Cuando el parámetro *pszContainer* de la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) es **null**, algunos de los proveedores de servicios criptográficos de Microsoft usan el nombre de inicio de sesión del usuario que ha iniciado sesión actualmente como el nombre del contenedor de claves.</span><span class="sxs-lookup"><span data-stu-id="75646-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="75646-109">MAXUIDLEN especifica el número máximo de caracteres, incluido el carácter **nulo** de terminación, que estos proveedores usarán para el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="75646-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="75646-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75646-110">Requirements</span></span>



| <span data-ttu-id="75646-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="75646-111">Requirement</span></span> | <span data-ttu-id="75646-112">Value</span><span class="sxs-lookup"><span data-stu-id="75646-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75646-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75646-113">Minimum supported client</span></span><br/> | <span data-ttu-id="75646-114">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="75646-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75646-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75646-115">Minimum supported server</span></span><br/> | <span data-ttu-id="75646-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="75646-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75646-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75646-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="75646-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="75646-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75646-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="75646-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75646-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="75646-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="75646-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="75646-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




