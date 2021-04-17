---
description: Cuando una aplicación usa la API de administración de credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por parte del sistema operativo o de la aplicación.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nombre de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652905"
---
# <a name="user-name-formats"></a><span data-ttu-id="e8f7a-103">Formatos de nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="e8f7a-103">User Name Formats</span></span>

<span data-ttu-id="e8f7a-104">Cuando una aplicación usa la API de administración de credenciales para solicitar credenciales, se espera que el usuario escriba información que se pueda validar, ya sea por parte del sistema operativo o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="e8f7a-105">El usuario puede especificar la información de las credenciales de dominio en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="e8f7a-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="e8f7a-106">Nombre principal del usuario</span><span class="sxs-lookup"><span data-stu-id="e8f7a-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="e8f7a-107">Nombre de inicio de sesión de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="e8f7a-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="e8f7a-108">Nombre principal del usuario</span><span class="sxs-lookup"><span data-stu-id="e8f7a-108">User Principal Name</span></span>

<span data-ttu-id="e8f7a-109">[*El formato de nombre principal de usuario*](../secgloss/u-gly.md) (UPN) se usa para especificar un nombre de estilo de Internet, como <b>UserName@Example.Microsoft.com</b> .</span><span class="sxs-lookup"><span data-stu-id="e8f7a-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="e8f7a-110">En la tabla siguiente se resumen las partes de un UPN.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="e8f7a-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e8f7a-111">Part</span></span>                                                        | <span data-ttu-id="e8f7a-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8f7a-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="e8f7a-113">Nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-113">User account name.</span></span> <span data-ttu-id="e8f7a-114">También se conoce como nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="e8f7a-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="e8f7a-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="e8f7a-116">Separador.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-116">Separator.</span></span> <span data-ttu-id="e8f7a-117">Un literal de carácter, el signo de arroba (@).</span><span class="sxs-lookup"><span data-stu-id="e8f7a-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="e8f7a-118">Sufijo UPN.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-118">UPN suffix.</span></span> <span data-ttu-id="e8f7a-119">También se conoce como nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="e8f7a-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="e8f7a-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="e8f7a-121">Un UPN puede definirse implícita o explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="e8f7a-122">Un UPN implícito tiene el formato <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="e8f7a-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="e8f7a-123">Un UPN implícito siempre está asociado a la cuenta del usuario, incluso si no se ha definido un UPN explícito.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="e8f7a-124">Un UPN explícito tiene el formato <i><b>Name@Suffix</b></i> , donde el administrador define explícitamente las cadenas de nombre y sufijo.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="e8f7a-125">Nombre de inicio de sesión Down-Level</span><span class="sxs-lookup"><span data-stu-id="e8f7a-125">Down-Level Logon Name</span></span>

<span data-ttu-id="e8f7a-126">El formato de nombre de inicio de sesión de nivel inferior se usa para especificar un dominio y una cuenta de usuario en ese dominio, por ejemplo, <i><b>dominio \\ nombreDeUsuario</b></i>.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="e8f7a-127">En la tabla siguiente se resumen las partes de un nombre de inicio de sesión de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="e8f7a-128">Parte</span><span class="sxs-lookup"><span data-stu-id="e8f7a-128">Part</span></span>                                                           | <span data-ttu-id="e8f7a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8f7a-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="e8f7a-130">Nombre de dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="e8f7a-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="e8f7a-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="e8f7a-132">Separador.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-132">Separator.</span></span> <span data-ttu-id="e8f7a-133">Un literal de carácter, la barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e8f7a-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="e8f7a-134">Nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-134">User account name.</span></span> <span data-ttu-id="e8f7a-135">También se conoce como nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e8f7a-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="e8f7a-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="e8f7a-136">*UserName*</span></span><br/> |



 

 

 
