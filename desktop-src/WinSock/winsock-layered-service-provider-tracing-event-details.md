---
description: Detalles de seguimiento de cambios de catálogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Detalles de seguimiento de cambios de catálogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155249"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="c0f7f-103">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="c0f7f-104">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="c0f7f-105">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="c0f7f-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="c0f7f-106">El seguimiento de eventos de cambio de catálogo Winsock para proveedores de servicios por capas (LSP) está relacionado con la instalación de LSP, la eliminación de LSP, la deshabilitación de LSP y las operaciones de restablecimiento del catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="c0f7f-107">Todos los eventos siguientes se escriben en el canal *Microsoft-Windows-Winsock-WS2HELP/Operational* , que es diferente del otro seguimiento de eventos de red Winsock registrado en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="c0f7f-108">A continuación se detalla cada uno de los eventos de LSP de Winsock de los que se puede realizar un seguimiento y se describen los parámetros y la información que se registran.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="c0f7f-109">Instalación de LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-109">LSP Install</span></span>

<span data-ttu-id="c0f7f-110">ID. de evento = 1</span><span class="sxs-lookup"><span data-stu-id="c0f7f-110">Event ID = 1</span></span>

<span data-ttu-id="c0f7f-111">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="c0f7f-111">Level = 4 (Information)</span></span>

<span data-ttu-id="c0f7f-112">Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de instalación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="c0f7f-113">Una entrada de protocolo se instala en el catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="c0f7f-114">Los parámetros siguientes se registran para un evento de instalación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="c0f7f-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0f7f-115">Parameter</span></span>                                                                                                | <span data-ttu-id="c0f7f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0f7f-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f7f-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="c0f7f-118">El nombre del LSP tal como se obtuvo del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="c0f7f-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo</span><span class="sxs-lookup"><span data-stu-id="c0f7f-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="c0f7f-120">El catálogo Winsock (32 bits o 64 bits) en el que se está instalando el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="c0f7f-121">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="c0f7f-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="c0f7f-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="c0f7f-123">El nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="c0f7f-124"><span id="GUID"></span><span id="guid"></span>VOLUMEN</span><span class="sxs-lookup"><span data-stu-id="c0f7f-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="c0f7f-125">Valor GUID del proveedor de transporte Winsock en el que se está instalando el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="c0f7f-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría</span><span class="sxs-lookup"><span data-stu-id="c0f7f-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="c0f7f-127">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="c0f7f-128">Desinstalación de LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-128">LSP Uninstall</span></span>

<span data-ttu-id="c0f7f-129">ID. de evento = 2</span><span class="sxs-lookup"><span data-stu-id="c0f7f-129">Event ID = 2</span></span>

<span data-ttu-id="c0f7f-130">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="c0f7f-130">Level = 4 (Information)</span></span>

<span data-ttu-id="c0f7f-131">Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de desinstalación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="c0f7f-132">Se quita una entrada de protocolo del catálogo de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="c0f7f-133">Los parámetros siguientes se registran para un evento de desinstalación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="c0f7f-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0f7f-134">Parameter</span></span>                                                                                                | <span data-ttu-id="c0f7f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0f7f-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f7f-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="c0f7f-137">Nombre del LSP obtenido del miembro **szProtocol** de la estructura de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="c0f7f-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo</span><span class="sxs-lookup"><span data-stu-id="c0f7f-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="c0f7f-139">El catálogo Winsock (32 bits o 64 bits) en el que se va a quitar el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="c0f7f-140">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="c0f7f-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="c0f7f-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="c0f7f-142">El nombre de archivo del módulo de la aplicación que realiza la llamada Remove de LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="c0f7f-143"><span id="GUID"></span><span id="guid"></span>VOLUMEN</span><span class="sxs-lookup"><span data-stu-id="c0f7f-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="c0f7f-144">Valor GUID del proveedor de transporte Winsock del que se quita el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="c0f7f-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría</span><span class="sxs-lookup"><span data-stu-id="c0f7f-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="c0f7f-146">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="c0f7f-147">Deshabilitación de LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-147">LSP Disable</span></span>

<span data-ttu-id="c0f7f-148">ID. de evento = 3</span><span class="sxs-lookup"><span data-stu-id="c0f7f-148">Event ID = 3</span></span>

<span data-ttu-id="c0f7f-149">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="c0f7f-149">Level = 4 (Information)</span></span>

<span data-ttu-id="c0f7f-150">Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de deshabilitación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="c0f7f-151">Una entrada de protocolo está deshabilitada en el catálogo de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="c0f7f-152">Los parámetros siguientes se registran para un evento de deshabilitación de LSP:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="c0f7f-153">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0f7f-153">Parameter</span></span>                                                                                                | <span data-ttu-id="c0f7f-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0f7f-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f7f-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP</span><span class="sxs-lookup"><span data-stu-id="c0f7f-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="c0f7f-156">Nombre del LSP tal y como se obtiene del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="c0f7f-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo</span><span class="sxs-lookup"><span data-stu-id="c0f7f-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="c0f7f-158">El catálogo Winsock (32 bits o 64 bits) en el que se deshabilita el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="c0f7f-159">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="c0f7f-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador</span><span class="sxs-lookup"><span data-stu-id="c0f7f-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="c0f7f-161">El nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="c0f7f-162"><span id="GUID"></span><span id="guid"></span>VOLUMEN</span><span class="sxs-lookup"><span data-stu-id="c0f7f-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="c0f7f-163">Valor GUID del proveedor de transporte Winsock en el que se va a deshabilitar el LSP.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="c0f7f-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría</span><span class="sxs-lookup"><span data-stu-id="c0f7f-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="c0f7f-165">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="c0f7f-166">Restablecimiento del catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="c0f7f-167">ID. de evento = 4</span><span class="sxs-lookup"><span data-stu-id="c0f7f-167">Event ID = 4</span></span>

<span data-ttu-id="c0f7f-168">Nivel = 4 (información)</span><span class="sxs-lookup"><span data-stu-id="c0f7f-168">Level = 4 (Information)</span></span>

<span data-ttu-id="c0f7f-169">Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de restablecimiento del catálogo Winsock:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="c0f7f-170">Se restablece el catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="c0f7f-171">Los parámetros siguientes se registran para un evento de restablecimiento del catálogo Winsock:</span><span class="sxs-lookup"><span data-stu-id="c0f7f-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="c0f7f-172">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0f7f-172">Parameter</span></span>                                                                                        | <span data-ttu-id="c0f7f-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0f7f-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f7f-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo</span><span class="sxs-lookup"><span data-stu-id="c0f7f-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="c0f7f-175">Catálogo Winsock (32 bits o 64 bits) que se va a restablecer.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="c0f7f-176">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="c0f7f-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c0f7f-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0f7f-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0f7f-178">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="c0f7f-179">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="c0f7f-180">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="c0f7f-181">Detalles de seguimiento de eventos de red Winsock</span><span class="sxs-lookup"><span data-stu-id="c0f7f-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
