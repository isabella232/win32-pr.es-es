---
description: Es el módulo de Windows que realiza el inicio de sesión interactivo para una sesión de inicio de sesión. El comportamiento de Winlogon se puede personalizar implementando y registrando un proveedor de credenciales.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon y proveedores de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001083"
---
# <a name="winlogon-and-credential-providers"></a><span data-ttu-id="ab499-104">Winlogon y proveedores de credenciales</span><span class="sxs-lookup"><span data-stu-id="ab499-104">Winlogon and Credential Providers</span></span>

<span data-ttu-id="ab499-105">[*Winlogon*](../secgloss/w-gly.md) es el módulo de Windows que realiza el inicio de sesión interactivo para una [*sesión de inicio*](../secgloss/l-gly.md)de sesión.</span><span class="sxs-lookup"><span data-stu-id="ab499-105">[*Winlogon*](../secgloss/w-gly.md) is the Windows module that performs interactive logon for a [*logon session*](../secgloss/l-gly.md).</span></span> <span data-ttu-id="ab499-106">El comportamiento de Winlogon se puede personalizar implementando y registrando un proveedor de credenciales.</span><span class="sxs-lookup"><span data-stu-id="ab499-106">Winlogon behavior can be customized by implementing and registering a Credential Provider.</span></span>

<span data-ttu-id="ab499-107">Para obtener información acerca de la implementación de un proveedor de credenciales, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ab499-107">For information about implementing a Credential Provider, see the following topics.</span></span>



| <span data-ttu-id="ab499-108">Tema</span><span class="sxs-lookup"><span data-stu-id="ab499-108">Topic</span></span>                                                                                                           | <span data-ttu-id="ab499-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab499-109">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab499-110">Experiencia de inicio de sesión Windows controlada por el proveedor de credenciales</span><span class="sxs-lookup"><span data-stu-id="ab499-110">Credential Provider driven Windows Logon Experience</span></span>](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | <span data-ttu-id="ab499-111">Información general de la arquitectura de los proveedores de credenciales y Winlogon y un proveedor de credenciales de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ab499-111">Overview of Winlogon and Credential Provider architecture and a sample Credential Provider.</span></span><br/> |
| [<span data-ttu-id="ab499-112">Interfaces de Shell</span><span class="sxs-lookup"><span data-stu-id="ab499-112">Shell Interfaces</span></span>](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | <span data-ttu-id="ab499-113">Referencia de la interfaz del proveedor de credenciales.</span><span class="sxs-lookup"><span data-stu-id="ab499-113">Credential Provider interface reference.</span></span><br/>                                                    |
| [<span data-ttu-id="ab499-114">Proveedores de credenciales en Windows 10</span><span class="sxs-lookup"><span data-stu-id="ab499-114">Credential Providers in Windows 10</span></span>](credential-providers-in-windows.md)<br/>                            | <span data-ttu-id="ab499-115">Proveedores de credenciales de terceros y proveedores de credenciales del sistema en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ab499-115">Third-party credential providers and system credential providers in Windows 10.</span></span><br/>             |



 

<span data-ttu-id="ab499-116">Para obtener una implementación de proveedor de credenciales de ejemplo, vea el ejemplo que se encuentra en el directorio de instalación de Windows SDK en \\ Samples \\ Security \\ CredentialProvider.</span><span class="sxs-lookup"><span data-stu-id="ab499-116">For a sample Credential Provider implementation, see the sample located in the Windows SDK installation directory under \\Samples\\Security\\CredentialProvider.</span></span>

<span data-ttu-id="ab499-117">**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales.</span><span class="sxs-lookup"><span data-stu-id="ab499-117">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span> <span data-ttu-id="ab499-118">Para obtener información acerca de cómo personalizar Winlogon, consulte [Winlogon y Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="ab499-118">For information about customizing Winlogon, see [Winlogon and GINA](winlogon-and-gina.md).</span></span>

 

 
