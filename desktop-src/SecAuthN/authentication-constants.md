---
description: Muestra las constantes utilizadas para las API de autenticación de Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes de autenticación (autenticación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648575"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="80067-103">Constantes de autenticación (autenticación)</span><span class="sxs-lookup"><span data-stu-id="80067-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="80067-104">Constantes de administración de credenciales</span><span class="sxs-lookup"><span data-stu-id="80067-104">Credentials Management Constants</span></span>

<span data-ttu-id="80067-105">La administración de credenciales utiliza las siguientes constantes para especificar tamaños de cadena máximos.</span><span class="sxs-lookup"><span data-stu-id="80067-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="80067-106">Constante</span><span class="sxs-lookup"><span data-stu-id="80067-106">Constant</span></span>                                        | <span data-ttu-id="80067-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="80067-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80067-108">\_longitud máxima del \_ mensaje \_ de CREDUI</span><span class="sxs-lookup"><span data-stu-id="80067-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="80067-109">Número máximo de caracteres para el miembro **pszMessageText** de una estructura de [**\_ información de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="80067-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="80067-110">CREDUI \_ longitud máxima del \_ título \_</span><span class="sxs-lookup"><span data-stu-id="80067-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="80067-111">Número máximo de caracteres para el miembro **pszCaptionText** de una estructura de [**\_ información de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="80067-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="80067-112">\_longitud máxima \_ de \_ destino \_ genérico de CREDUI</span><span class="sxs-lookup"><span data-stu-id="80067-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="80067-113">Número máximo de caracteres de una cadena que especifica un nombre de destino.</span><span class="sxs-lookup"><span data-stu-id="80067-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="80067-114">\_longitud máxima \_ de \_ destino de dominio \_ de CREDUI</span><span class="sxs-lookup"><span data-stu-id="80067-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="80067-115">Número máximo de caracteres de una cadena que especifica un nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="80067-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="80067-116">\_longitud máxima de \_ nombre de usuario de CREDUI \_</span><span class="sxs-lookup"><span data-stu-id="80067-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="80067-117">Número máximo de caracteres de una cadena que especifica un nombre de cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="80067-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="80067-118">CREDUI \_ longitud máxima de la \_ contraseña \_</span><span class="sxs-lookup"><span data-stu-id="80067-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="80067-119">Número máximo de caracteres de una cadena que especifica una contraseña.</span><span class="sxs-lookup"><span data-stu-id="80067-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="80067-120">Valores definidos de Gina</span><span class="sxs-lookup"><span data-stu-id="80067-120">Gina Defined Values</span></span>

<span data-ttu-id="80067-121">Las funciones de la interfaz [*Gina*](/windows/desktop/SecGloss/g-gly) y las funciones de compatibilidad con [*Winlogon*](/windows/desktop/SecGloss/w-gly) usan los siguientes valores definidos.</span><span class="sxs-lookup"><span data-stu-id="80067-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="80067-122">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80067-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="80067-123">Value</span><span class="sxs-lookup"><span data-stu-id="80067-123">Value</span></span>                                                              | <span data-ttu-id="80067-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="80067-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80067-125">**WLX \_ opción de inicio de sesión \_ \_ XXX**</span><span class="sxs-lookup"><span data-stu-id="80067-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="80067-126">Contiene opciones de inicio de sesión predefinidas.</span><span class="sxs-lookup"><span data-stu-id="80067-126">Contains predefined logon options.</span></span> <span data-ttu-id="80067-127">Lo usa el parámetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="80067-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="80067-128">**WLX \_ SAS \_ tipo \_ XXX**</span><span class="sxs-lookup"><span data-stu-id="80067-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="80067-129">Define un tipo de SAS específico.</span><span class="sxs-lookup"><span data-stu-id="80067-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

