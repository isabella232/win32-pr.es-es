---
description: Detalles del seguimiento de cambios del catálogo de Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Detalles del seguimiento de cambios del catálogo de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967248"
---
# <a name="winsock-catalog-change-tracing-details"></a>Detalles del seguimiento de cambios del catálogo de Winsock

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows de filtrado.](../fwp/windows-filtering-platform-start-page.md)

 

El seguimiento de eventos de cambio de catálogo de Winsock para proveedores de servicios por capas (LSP) está relacionado con las operaciones de instalación de LSP, eliminación de LSP, deshabilitación de LSP y restablecimiento del catálogo de Winsock. Todos los eventos siguientes se escriben en el canal *Microsoft-Windows-Winsock-WS2HELP/Operational,* que es diferente del otro seguimiento de eventos de red de Winsock registrado en Windows Vista y versiones posteriores.

A continuación se detalla cada uno de los eventos de Winsock LSP de los que se puede realizar un seguimiento y se describen los parámetros y la información que se registran.

## <a name="lsp-install"></a>Instalación de LSP

Id. de evento = 1

Nivel = 4 (información)

Se sigue el seguimiento de los siguientes eventos de Winsock LSP para una operación de instalación de LSP:

-   Se instala una entrada de protocolo en el catálogo winsock.

Los parámetros siguientes se registran para un evento de instalación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre de LSP<br/>     | Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a instalar.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | El catálogo winsock (32 o 64 bits) donde se instala el LSP. Se trata de un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | Nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valor GUID del proveedor de transporte winsock en el que se está instalando el LSP.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | Miembro **dwCatalogEntryId** de la [**estructura INFO \_ de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a instalar.<br/>                                |



 

## <a name="lsp-uninstall"></a>Desinstalación de LSP

Id. de evento = 2

Nivel = 4 (información)

Se sigue el seguimiento de los siguientes eventos de Winsock LSP para una operación de desinstalación de LSP:

-   Se quita una entrada de protocolo del catálogo winsock.

Los parámetros siguientes se registran para un evento de desinstalación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre de LSP<br/>     | Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | Catálogo winsock (32 o 64 bits) donde se quita el LSP. Se trata de un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | Nombre de archivo del módulo de la aplicación que realiza la llamada de eliminación de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valor GUID del proveedor de transporte winsock del que se quita el LSP.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | Miembro **dwCatalogEntryId** de la estructura [**INFO \_ de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.<br/>                                |



 

## <a name="lsp-disable"></a>LSP Disable

Id. de evento = 3

Nivel = 4 (información)

Se sigue el seguimiento de los siguientes eventos de Winsock LSP para una operación de deshabilitación de LSP:

-   Una entrada de protocolo está deshabilitada en el catálogo winsock.

Los parámetros siguientes se registran para un evento de deshabilitación de LSP:



| Parámetro                                                                                                | Descripción                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nombre de LSP<br/>     | Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está deshabilitando.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | Catálogo de Winsock (32 o 64 bits) donde se deshabilita el LSP. Se trata de un valor entero que es 32 o 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | Nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>GUID<br/>                                            | Valor GUID del proveedor de transporte winsock donde se deshabilita el LSP.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoría<br/>     | Miembro **dwCatalogEntryId de** la estructura [**INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se deshabilita.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Restablecimiento del catálogo de Winsock

Id. de evento = 4

Nivel = 4 (información)

Se sigue el seguimiento de los siguientes eventos de Winsock LSP para una operación de restablecimiento del catálogo de Winsock:

-   Se restablece el catálogo de Winsock.

Los parámetros siguientes se registran para un evento de restablecimiento del catálogo de Winsock:



| Parámetro                                                                                        | Descripción                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/> | Catálogo de Winsock (32 o 64 bits) que se va a restablecer. Se trata de un valor entero que es 32 o 64.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles del seguimiento de eventos de Winsock Network](winsock-tracing-event-details.md)
</dt> </dl>

 

 
