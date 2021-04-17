---
description: Explica cómo cambiar los privilegios de un token mediante las funciones AdjustTokenPrivileges y CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Cambiar los privilegios de un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669670"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="2fc69-103">Cambiar los privilegios de un token</span><span class="sxs-lookup"><span data-stu-id="2fc69-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="2fc69-104">Puede cambiar los privilegios en un token principal o de suplantación de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="2fc69-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="2fc69-105">Habilitar o deshabilitar privilegios mediante la función [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="2fc69-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="2fc69-106">Restrinja o quite privilegios mediante la función [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .</span><span class="sxs-lookup"><span data-stu-id="2fc69-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="2fc69-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) no puede agregar ni quitar privilegios del token.</span><span class="sxs-lookup"><span data-stu-id="2fc69-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="2fc69-108">Solo puede habilitar los privilegios existentes que están deshabilitados actualmente o deshabilitar los privilegios existentes que están habilitados actualmente.</span><span class="sxs-lookup"><span data-stu-id="2fc69-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="2fc69-109">Para obtener ejemplos, vea [habilitar y deshabilitar privilegios en C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="2fc69-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="2fc69-110">Para asignar privilegios a una cuenta de usuario, consulte [asignación de privilegios a una cuenta](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="2fc69-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="2fc69-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) tiene funcionalidades más amplias, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2fc69-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="2fc69-112">Quitar un privilegio.</span><span class="sxs-lookup"><span data-stu-id="2fc69-112">Removing a privilege.</span></span> <span data-ttu-id="2fc69-113">Tenga en cuenta que quitar un privilegio no es lo mismo que deshabilitar uno.</span><span class="sxs-lookup"><span data-stu-id="2fc69-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="2fc69-114">Una vez que se quita un privilegio de un token, no se puede devolver.</span><span class="sxs-lookup"><span data-stu-id="2fc69-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="2fc69-115">Adjuntando el atributo de solo denegación a los SID en el token.</span><span class="sxs-lookup"><span data-stu-id="2fc69-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="2fc69-116">Esto tiene el efecto de no permitir cuentas o grupos específicos, por ejemplo, denegar el acceso de eliminación del grupo todos a un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="2fc69-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="2fc69-117">Para obtener más información sobre cómo restringir los SID, consulte [atributos de SID en un token de acceso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="2fc69-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="2fc69-118">Especificación de una lista de los SID restrictivos en el token.</span><span class="sxs-lookup"><span data-stu-id="2fc69-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="2fc69-119">Para obtener información acerca de cómo restringir los SID, consulte [tokens restringidos](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="2fc69-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
