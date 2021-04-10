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
# <a name="winsock-catalog-change-tracing-details"></a>Detalles de seguimiento de cambios de catálogo Winsock

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El seguimiento de eventos de cambio de catálogo Winsock para proveedores de servicios por capas (LSP) está relacionado con la instalación de LSP, la eliminación de LSP, la deshabilitación de LSP y las operaciones de restablecimiento del catálogo Winsock. Todos los eventos siguientes se escriben en el canal *Microsoft-Windows-Winsock-WS2HELP/Operational* , que es diferente del otro seguimiento de eventos de red Winsock registrado en Windows Vista y versiones posteriores.

A continuación se detalla cada uno de los eventos de LSP de Winsock de los que se puede realizar un seguimiento y se describen los parámetros y la información que se registran.

## <a name="lsp-install"></a>Instalación de LSP

ID. de evento = 1

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de instalación de LSP:

-   Una entrada de protocolo se instala en el catálogo Winsock.

Los parámetros siguientes se registran para un evento de instalación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP<br/>     | El nombre del LSP tal como se obtuvo del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | El catálogo Winsock (32 bits o 64 bits) en el que se está instalando el LSP. Es un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | El nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>VOLUMEN<br/>                                            | Valor GUID del proveedor de transporte Winsock en el que se está instalando el LSP.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.<br/>                                |



 

## <a name="lsp-uninstall"></a>Desinstalación de LSP

ID. de evento = 2

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de desinstalación de LSP:

-   Se quita una entrada de protocolo del catálogo de Winsock.

Los parámetros siguientes se registran para un evento de desinstalación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP<br/>     | Nombre del LSP obtenido del miembro **szProtocol** de la estructura de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | El catálogo Winsock (32 bits o 64 bits) en el que se va a quitar el LSP. Es un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | El nombre de archivo del módulo de la aplicación que realiza la llamada Remove de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>VOLUMEN<br/>                                            | Valor GUID del proveedor de transporte Winsock del que se quita el LSP.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.<br/>                                |



 

## <a name="lsp-disable"></a>Deshabilitación de LSP

ID. de evento = 3

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de deshabilitación de LSP:

-   Una entrada de protocolo está deshabilitada en el catálogo de Winsock.

Los parámetros siguientes se registran para un evento de deshabilitación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre del LSP<br/>     | Nombre del LSP tal y como se obtiene del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | El catálogo Winsock (32 bits o 64 bits) en el que se deshabilita el LSP. Es un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | El nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>VOLUMEN<br/>                                            | Valor GUID del proveedor de transporte Winsock en el que se va a deshabilitar el LSP.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Restablecimiento del catálogo Winsock

ID. de evento = 4

Nivel = 4 (información)

Se realiza un seguimiento de los siguientes eventos de LSP de Winsock para una operación de restablecimiento del catálogo Winsock:

-   Se restablece el catálogo Winsock.

Los parámetros siguientes se registran para un evento de restablecimiento del catálogo Winsock:



| Parámetro                                                                                        | Descripción                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/> | Catálogo Winsock (32 bits o 64 bits) que se va a restablecer. Es un valor entero que es 32 o 64.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles de seguimiento de eventos de red Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
