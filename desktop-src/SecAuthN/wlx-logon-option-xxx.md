---
description: Los valores son usados por el parámetro dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361026"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="3c818-103">WLX \_ opción de inicio de sesión \_ \_ XXX</span><span class="sxs-lookup"><span data-stu-id="3c818-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="3c818-104">\[La \_ constante XXX de la opción de inicio de sesión WLX ya \_ \_ no está disponible para su uso en Windows Server 2008 y Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="3c818-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="3c818-105">El parámetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)usa los valores de la **opción de inicio de \_ sesión \_ \_ WLX** .</span><span class="sxs-lookup"><span data-stu-id="3c818-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="3c818-106">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3c818-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="3c818-107">Tras un inicio de sesión correcto, el archivo DLL de GINA puede usar este valor para especificar la opción siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c818-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="3c818-108">Constante</span><span class="sxs-lookup"><span data-stu-id="3c818-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="3c818-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c818-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="3c818-110"><dt>**WLX \_ Inicio de sesión \_ \_ no opt ningún \_ Perfil**</dt></span><span class="sxs-lookup"><span data-stu-id="3c818-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="3c818-111">Especifica que Winlogon no debe cargar un perfil para el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3c818-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="3c818-112">En este caso, el archivo DLL de GINA cargará el perfil o el usuario no necesita un perfil.</span><span class="sxs-lookup"><span data-stu-id="3c818-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3c818-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c818-113">Requirements</span></span>



| <span data-ttu-id="3c818-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c818-114">Requirement</span></span> | <span data-ttu-id="3c818-115">Value</span><span class="sxs-lookup"><span data-stu-id="3c818-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c818-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c818-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c818-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3c818-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c818-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c818-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c818-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c818-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c818-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3c818-120">End of client support</span></span><br/>    | <span data-ttu-id="3c818-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c818-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="3c818-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3c818-122">End of server support</span></span><br/>    | <span data-ttu-id="3c818-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c818-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="3c818-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c818-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c818-125"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c818-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




