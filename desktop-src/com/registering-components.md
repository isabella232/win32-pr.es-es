---
title: Registrar componentes
description: Registrar componentes
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078409"
---
# <a name="registering-components"></a><span data-ttu-id="1e173-103">Registrar componentes</span><span class="sxs-lookup"><span data-stu-id="1e173-103">Registering Components</span></span>

<span data-ttu-id="1e173-104">Cuando se instalan los siguientes tipos de aplicaciones, se debe agregar información de instalación al registro, normalmente a través de un programa de instalación:</span><span class="sxs-lookup"><span data-stu-id="1e173-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="1e173-105">Aplicaciones de servidor</span><span class="sxs-lookup"><span data-stu-id="1e173-105">Server applications</span></span>
-   <span data-ttu-id="1e173-106">Aplicaciones de contenedor/servidor</span><span class="sxs-lookup"><span data-stu-id="1e173-106">Container/server applications</span></span>
-   <span data-ttu-id="1e173-107">Aplicaciones contenedoras que permiten la vinculación a objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="1e173-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="1e173-108">Para las tres instancias, registre la información de la biblioteca COM (DLL) y la información específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1e173-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="1e173-109">El archivo DLL registra la información de todos sus componentes mediante la exportación de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="1e173-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="1e173-110">Utilice las siguientes funciones para registrar y anular el registro de un componente:</span><span class="sxs-lookup"><span data-stu-id="1e173-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="1e173-111">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1e173-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="1e173-112">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1e173-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="1e173-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="1e173-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="1e173-114">**RegEnumKeyEx**</span><span class="sxs-lookup"><span data-stu-id="1e173-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="1e173-115">**RegDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="1e173-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="1e173-116">**RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="1e173-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="1e173-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e173-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e173-118">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="1e173-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 