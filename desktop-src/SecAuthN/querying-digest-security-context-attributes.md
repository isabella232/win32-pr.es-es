---
description: La función QueryContextAttributes (síntesis) proporciona información sobre la configuración actual de un contexto de seguridad.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consultar los atributos de contexto de seguridad implícita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001858"
---
# <a name="querying-digest-security-context-attributes"></a><span data-ttu-id="22761-103">Consultar los atributos de contexto de seguridad implícita</span><span class="sxs-lookup"><span data-stu-id="22761-103">Querying Digest Security Context Attributes</span></span>

<span data-ttu-id="22761-104">La función [**QueryContextAttributes (síntesis)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) proporciona información sobre la configuración actual de un [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="22761-104">The [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) function provides information about the current settings of a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="22761-105">Microsoft Digest admite la consulta de los siguientes atributos de contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="22761-105">Microsoft Digest supports querying the following security context attributes.</span></span>



| <span data-ttu-id="22761-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="22761-106">Attribute</span></span>                   | <span data-ttu-id="22761-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="22761-107">Description</span></span>                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22761-108">información de clave de SECPKG \_ ATTR \_ \_</span><span class="sxs-lookup"><span data-stu-id="22761-108">SECPKG\_ATTR\_KEY\_INFO</span></span>     | <span data-ttu-id="22761-109">Información relacionada con los algoritmos de firma y cifrado en uso.</span><span class="sxs-lookup"><span data-stu-id="22761-109">Information relating to the signing and encryption algorithms in use.</span></span>                                                                                                                                   |
| <span data-ttu-id="22761-110">información de paquete de SECPKG \_ ATTR \_ \_</span><span class="sxs-lookup"><span data-stu-id="22761-110">SECPKG\_ATTR\_PACKAGE\_INFO</span></span> | <span data-ttu-id="22761-111">Información general relativa a Microsoft Digest, como el tamaño máximo del token permitido por el [*paquete de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="22761-111">General information pertaining to Microsoft Digest, such as the maximum token size permitted by the [*security package*](../secgloss/s-gly.md).</span></span> |
| <span data-ttu-id="22761-112">tamaños de SECPKG \_ ATTR \_</span><span class="sxs-lookup"><span data-stu-id="22761-112">SECPKG\_ATTR\_SIZES</span></span>         | <span data-ttu-id="22761-113">Los tamaños máximos permitidos para los datos relacionados con mensajes, como las firmas.</span><span class="sxs-lookup"><span data-stu-id="22761-113">The maximum sizes permitted for message-related data such as signatures.</span></span>                                                                                                                                |



 

 

 
