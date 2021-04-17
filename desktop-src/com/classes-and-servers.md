---
title: Clases y servidores
description: Clases y servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421464"
---
# <a name="classes-and-servers"></a><span data-ttu-id="38cec-103">Clases y servidores</span><span class="sxs-lookup"><span data-stu-id="38cec-103">Classes and Servers</span></span>

<span data-ttu-id="38cec-104">COM utiliza **\_ las clases HKEY \_ raíz** para la configuración de todo el equipo, pero también permite la configuración por usuario de CLSID para una mayor seguridad y flexibilidad.</span><span class="sxs-lookup"><span data-stu-id="38cec-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="38cec-105">COM consulta primero **\_ \_ \\ \\ las clases de software de usuario actuales de HKEY** antes de buscar en **HKEY \_ classes \_ root**.</span><span class="sxs-lookup"><span data-stu-id="38cec-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="38cec-106">COM mantiene la información de todo el equipo relacionada con los CLSID en **\_ las clases HKEY \_ raíz \\ CLSID** y mantiene la información de clase por usuario en **HKEY \_ Current \_ User \\ \\ classes \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="38cec-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="38cec-107">Los servidores COM admiten el registro automático.</span><span class="sxs-lookup"><span data-stu-id="38cec-107">COM servers support self-registration.</span></span> <span data-ttu-id="38cec-108">Para un servidor en proceso, esto significa que el archivo DLL debe exportar las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="38cec-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="38cec-109">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="38cec-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="38cec-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="38cec-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="38cec-111">Debe exportar explícitamente estas funciones mediante un archivo de definición de módulo, modificadores del enlazador o directivas de compilador.</span><span class="sxs-lookup"><span data-stu-id="38cec-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="38cec-112">El almacén de clases utiliza estas funciones para configurar el registro local después de descargar el archivo en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="38cec-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="38cec-113">Además del almacén de clases, otras funciones también se usan en otros entornos para instalar servidores en equipos host.</span><span class="sxs-lookup"><span data-stu-id="38cec-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38cec-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38cec-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38cec-115">Registro de aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="38cec-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 