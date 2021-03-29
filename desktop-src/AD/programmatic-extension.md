---
title: Extensión de programación
description: Las extensiones de programación tienen varios méritos; sin embargo, una aplicación es opaca; el administrador debe confiar en la documentación incluida en la aplicación de instalación.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extensión de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773117"
---
# <a name="programmatic-extension"></a><span data-ttu-id="41c64-104">Extensión de programación</span><span class="sxs-lookup"><span data-stu-id="41c64-104">Programmatic Extension</span></span>

<span data-ttu-id="41c64-105">La ventaja de un archivo LDIF es que el administrador puede examinar su función.</span><span class="sxs-lookup"><span data-stu-id="41c64-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="41c64-106">Sin embargo, el esquema también se puede extender mediante programación.</span><span class="sxs-lookup"><span data-stu-id="41c64-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="41c64-107">Las extensiones de programación tienen varios méritos, pero una aplicación es opaca; el administrador debe confiar en la documentación incluida en la aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="41c64-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="41c64-108">El uso de extensiones de esquema mediante programación puede ser una barrera para la implementación de aplicaciones que las usan.</span><span class="sxs-lookup"><span data-stu-id="41c64-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="41c64-109">Una extensión de programación es invariable. es un archivo ejecutable de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="41c64-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="41c64-110">No se puede alterar el binario, a diferencia de un archivo LDIF o. csv, que se puede editar de forma inadvertida o malintencionada.</span><span class="sxs-lookup"><span data-stu-id="41c64-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="41c64-111">Las ventajas de un archivo LDIF incluyen:</span><span class="sxs-lookup"><span data-stu-id="41c64-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="41c64-112">Las aplicaciones pueden detectar y recuperarse de errores y proporcionar comentarios de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="41c64-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="41c64-113">Las aplicaciones pueden administrar Unicode sin tener que recurrir a la codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="41c64-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="41c64-114">Las aplicaciones pueden aprovechar Windows Installer API de instalación.</span><span class="sxs-lookup"><span data-stu-id="41c64-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="41c64-115">Las aplicaciones se pueden firmar para establecer la autenticidad.</span><span class="sxs-lookup"><span data-stu-id="41c64-115">Applications can be signed to establish authenticity.</span></span>

 

 




