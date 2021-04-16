---
description: Al crear un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante el uso de un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Usar tres nombres principales de parte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666461"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="9edc6-103">Usar tres nombres principales de parte</span><span class="sxs-lookup"><span data-stu-id="9edc6-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="9edc6-104">Al crear un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP), no debe permitir que el cliente unido a un dominio se autentique en un controlador de dominio mediante el uso de un nombre de proveedor de servicios (SPN) de dos partes con el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="9edc6-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="9edc6-105"><*Protocolo* >/< de *nombre de host*></span><span class="sxs-lookup"><span data-stu-id="9edc6-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="9edc6-106">Un cliente debe autenticarse siempre especificando el dominio.</span><span class="sxs-lookup"><span data-stu-id="9edc6-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="9edc6-107"><*Protocolo* >/< de *nombre* >/< de host *nombre de dominio*></span><span class="sxs-lookup"><span data-stu-id="9edc6-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="9edc6-108">Un cliente unido a un dominio que inicia sesión con un SPN de dos partes puede suplantar al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="9edc6-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="9edc6-109">Si permite dos SPN de partes, debe crear una entrada de registro que contenga información suficiente para permitir que el administrador identifique al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9edc6-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



