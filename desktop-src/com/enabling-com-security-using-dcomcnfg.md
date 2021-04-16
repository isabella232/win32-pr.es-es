---
title: Habilitar la seguridad COM mediante DCOMCNFG
description: Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695262"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="6facc-103">Habilitar la seguridad COM mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="6facc-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="6facc-104">Dcomcnfg.exe proporciona una interfaz de usuario para modificar algunos valores de configuración del Registro.</span><span class="sxs-lookup"><span data-stu-id="6facc-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="6facc-105">Mediante el uso de Dcomcnfg.exe, puede habilitar la seguridad en todo el equipo o en todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="6facc-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="6facc-106">Puede habilitar la seguridad de un equipo determinado para que cuando un proceso no proporcione su propia configuración de seguridad, ya sea mediante programación o a través de valores del registro, se utilicen los valores establecidos por Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="6facc-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="6facc-107">También puede usar Dcomcnfg.exe para habilitar la seguridad solo para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="6facc-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="6facc-108">Al habilitar la seguridad, hay dos tareas principales que debe realizar:</span><span class="sxs-lookup"><span data-stu-id="6facc-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="6facc-109">Establezca un nivel de autenticación que no sea ninguno.</span><span class="sxs-lookup"><span data-stu-id="6facc-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="6facc-110">Establezca permisos, incluidos los permisos de acceso y de inicio.</span><span class="sxs-lookup"><span data-stu-id="6facc-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="6facc-111">Los pasos que se llevan a cabo para realizar estas tareas dependen de si se habilita la seguridad para todo el equipo o solo para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="6facc-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="6facc-112">Además, es posible que desee establecer otros valores para el equipo o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6facc-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="6facc-113">Debe ser un administrador para ejecutar Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="6facc-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="6facc-114">En los temas siguientes se proporcionan procedimientos paso a paso para establecer la seguridad con Dcomcnfg.exe:</span><span class="sxs-lookup"><span data-stu-id="6facc-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="6facc-115">Establecer la seguridad de System-Wide mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="6facc-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="6facc-116">Configuración de la seguridad de Processwide mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="6facc-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="6facc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6facc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6facc-118">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="6facc-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="6facc-119">Desactivar la seguridad</span><span class="sxs-lookup"><span data-stu-id="6facc-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




