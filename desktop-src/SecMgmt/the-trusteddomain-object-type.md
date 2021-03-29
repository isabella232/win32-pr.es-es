---
description: Los sistemas basados en Windows pueden tener varias instancias del tipo de objeto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: El tipo de objeto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809295"
---
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="4d38d-103">El tipo de objeto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="4d38d-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="4d38d-104">Los sistemas basados en Windows pueden tener varias instancias del tipo de objeto [**TrustedDomain**](trusteddomain-object.md) .</span><span class="sxs-lookup"><span data-stu-id="4d38d-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="4d38d-105">Los objetos **TrustedDomain** tienen dos campos que deben ser únicos entre todos los objetos **TrustedDomain** :</span><span class="sxs-lookup"><span data-stu-id="4d38d-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="4d38d-106">Nombre del [ **TrustedDomain**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="4d38d-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="4d38d-107">El [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) de [**TrustedDomain**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="4d38d-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="4d38d-108">Se rechazará el intento de crear un nuevo objeto **TrustedDomain** con un nombre o SID que ya esté en uso por otro objeto **TrustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="4d38d-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
