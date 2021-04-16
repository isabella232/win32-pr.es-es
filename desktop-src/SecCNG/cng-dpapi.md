---
description: Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) en Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI DE CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666260"
---
# <a name="cng-dpapi"></a><span data-ttu-id="2d70d-103">DPAPI DE CNG</span><span class="sxs-lookup"><span data-stu-id="2d70d-103">CNG DPAPI</span></span>

<span data-ttu-id="2d70d-104">Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2d70d-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="2d70d-105">La API está compuesta de dos funciones: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="2d70d-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="2d70d-106">DPAPI es parte de CryptoAPI y se ha diseñado para desarrolladores que sabían muy poco sobre el uso de la criptografía.</span><span class="sxs-lookup"><span data-stu-id="2d70d-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="2d70d-107">Las dos funciones se pueden usar para cifrar y descifrar los datos estáticos en un único equipo.</span><span class="sxs-lookup"><span data-stu-id="2d70d-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="2d70d-108">La informática en la nube, sin embargo, a menudo requiere que el contenido cifrado en un equipo se descifre en otro.</span><span class="sxs-lookup"><span data-stu-id="2d70d-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="2d70d-109">Por tanto, a partir de Windows 8, Microsoft amplió la idea de usar una API relativamente sencilla para abarcar escenarios de nube.</span><span class="sxs-lookup"><span data-stu-id="2d70d-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="2d70d-110">Esta nueva API, denominada DPAPI-NG, permite compartir de forma segura secretos (claves, contraseñas, material de clave) y mensajes mediante su protección en un conjunto de entidades de seguridad que se pueden usar para desprotegerlos en equipos diferentes después de la autenticación y autorización adecuadas.</span><span class="sxs-lookup"><span data-stu-id="2d70d-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="2d70d-111">Actualmente se admiten las siguientes entidades de seguridad:</span><span class="sxs-lookup"><span data-stu-id="2d70d-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="2d70d-112">Un grupo de un bosque de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d70d-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="2d70d-113">Credenciales Web.</span><span class="sxs-lookup"><span data-stu-id="2d70d-113">Web credentials.</span></span>

<span data-ttu-id="2d70d-114">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d70d-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2d70d-115">Proveedores de protección</span><span class="sxs-lookup"><span data-stu-id="2d70d-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="2d70d-116">Descriptores de protección</span><span class="sxs-lookup"><span data-stu-id="2d70d-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="2d70d-117">Formato de datos protegidos</span><span class="sxs-lookup"><span data-stu-id="2d70d-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="2d70d-118">DPAPI-NG se basa en CNG (Cryptography Next Generation) e incluye las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="2d70d-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="2d70d-119">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2d70d-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="2d70d-120">**NCryptCloseProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2d70d-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="2d70d-121">**NCryptProtectSecret**</span><span class="sxs-lookup"><span data-stu-id="2d70d-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="2d70d-122">**NCryptQueryProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="2d70d-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="2d70d-123">**NCryptRegisterProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="2d70d-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="2d70d-124">**NCryptStreamClose**</span><span class="sxs-lookup"><span data-stu-id="2d70d-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="2d70d-125">**NCryptStreamOpenToProtect**</span><span class="sxs-lookup"><span data-stu-id="2d70d-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="2d70d-126">**NCryptStreamOpenToUnprotect**</span><span class="sxs-lookup"><span data-stu-id="2d70d-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="2d70d-127">**NCryptStreamUpdate**</span><span class="sxs-lookup"><span data-stu-id="2d70d-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="2d70d-128">**NCryptUnprotectSecret**</span><span class="sxs-lookup"><span data-stu-id="2d70d-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
