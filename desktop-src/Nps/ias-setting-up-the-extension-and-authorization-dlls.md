---
title: Configuración de los archivos dll de extensión
description: En el inicio, NPS comprueba el registro para obtener una lista de archivos dll de terceros a los que llamar.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078071"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="a2fc1-103">Configuración de los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="a2fc1-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="a2fc1-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="a2fc1-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="a2fc1-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="a2fc1-107">En el inicio, NPS comprueba el registro para obtener una lista de archivos dll de terceros a los que llamar.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="a2fc1-108">Para configurar una DLL de autenticación o de autorización en un servidor NPS, enumere las rutas de acceso a los archivos dll en valores inferiores a la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="a2fc1-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="a2fc1-109">**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ Parameters\\**</span><span class="sxs-lookup"><span data-stu-id="a2fc1-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="a2fc1-110">Si no existen las claves **AuthSrv** y **Parameters** , créelos.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="a2fc1-111">El valor en el que se enumeran los archivos dll de extensión de autenticación es:</span><span class="sxs-lookup"><span data-stu-id="a2fc1-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="a2fc1-112">**ExtensionDLLs**</span><span class="sxs-lookup"><span data-stu-id="a2fc1-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="a2fc1-113">El valor en el que se enumeran los archivos dll de la extensión de autorización es:</span><span class="sxs-lookup"><span data-stu-id="a2fc1-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="a2fc1-114">**AuthorizationDLLs**</span><span class="sxs-lookup"><span data-stu-id="a2fc1-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="a2fc1-115">Los valores **ExtensionDLLs** y **AuthorizationDLLs** deben ser de tipo **reg \_ multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="a2fc1-116">Este tipo permite enumerar varios archivos dll.</span><span class="sxs-lookup"><span data-stu-id="a2fc1-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2fc1-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2fc1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2fc1-118">Invocar los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="a2fc1-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="a2fc1-119">Atributos de identificación de usuario</span><span class="sxs-lookup"><span data-stu-id="a2fc1-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 