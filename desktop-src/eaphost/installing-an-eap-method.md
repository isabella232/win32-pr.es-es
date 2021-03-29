---
title: Instalación de un método EAP
description: Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecuta EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790864"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="201e4-103">Instalación de un método EAP</span><span class="sxs-lookup"><span data-stu-id="201e4-103">Installing an EAP Method</span></span>

<span data-ttu-id="201e4-104">Siga las instrucciones siguientes para instalar un método EAP implementado por el usuario en un equipo cliente que ejecuta EAPHost.</span><span class="sxs-lookup"><span data-stu-id="201e4-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="201e4-105">Implemente [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para el archivo DLL del método EAP.</span><span class="sxs-lookup"><span data-stu-id="201e4-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="201e4-106">Estas funciones agregan y quitan las claves del registro adecuadas para el método EAP durante el proceso de instalación y (desinstalación).</span><span class="sxs-lookup"><span data-stu-id="201e4-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="201e4-107">Para obtener información sobre las claves del registro específicas asociadas a la instalación de un método EAP, consulte el tema [configuración del registro para métodos EAP](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="201e4-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="201e4-108">Instale el archivo DLL que contiene la implementación del método EAP con el siguiente comando de la consola.</span><span class="sxs-lookup"><span data-stu-id="201e4-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="201e4-109"> *&lt; Nombre &gt;* deregsvr32.exedll</span><span class="sxs-lookup"><span data-stu-id="201e4-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="201e4-110">Para desinstalar el archivo DLL, use el siguiente comando de la consola:</span><span class="sxs-lookup"><span data-stu-id="201e4-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="201e4-111">**regsvr32.exe** **/u** *&lt; nombre &gt; del archivo dll*</span><span class="sxs-lookup"><span data-stu-id="201e4-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="201e4-112">Reinicie el servicio EAPHost.</span><span class="sxs-lookup"><span data-stu-id="201e4-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="201e4-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="201e4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="201e4-114">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="201e4-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 