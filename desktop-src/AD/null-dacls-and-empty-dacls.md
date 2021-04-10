---
title: DACL NULL y listas DACL vacías (AD DS)
description: La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo nTSecurityDescriptor de cualquier objeto puede crear un riesgo de seguridad grave.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL NULL y listas DACL vacías
- DACL AD, NULL y Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995068"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="54662-105">DACL NULL y listas DACL vacías (AD DS)</span><span class="sxs-lookup"><span data-stu-id="54662-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="54662-106">La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de cualquier objeto puede crear un riesgo de seguridad grave.</span><span class="sxs-lookup"><span data-stu-id="54662-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="54662-107">Una DACL null concede acceso completo a cualquier usuario que lo solicite; la comprobación de seguridad normal no se realiza con respecto al objeto.</span><span class="sxs-lookup"><span data-stu-id="54662-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="54662-108">Una DACL null no se debería confundir con una DACL vacía.</span><span class="sxs-lookup"><span data-stu-id="54662-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="54662-109">Una DACL vacía es una DACL que se ha asignado y se ha inicializado correctamente y que no contiene entradas de control de acceso (ACE).</span><span class="sxs-lookup"><span data-stu-id="54662-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="54662-110">Una DACL vacía no concede ningún acceso al objeto al que se asigna.</span><span class="sxs-lookup"><span data-stu-id="54662-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="54662-111">Para obtener más información, vea [listas DACL nulas y listas DACL vacías](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="54662-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 