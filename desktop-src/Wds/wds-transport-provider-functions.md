---
title: Funciones del proveedor de transporte de WDS
description: Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779392"
---
# <a name="wds-transport-provider-functions"></a>Funciones del proveedor de transporte de WDS

Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.



| Función                                                                               | Descripción                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Cierra una secuencia de contenido especificada por un identificador.                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Cierra una instancia de un proveedor de contenido especificado por un identificador.                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Compara una instancia y un nombre de contenido especificados con un flujo de contenido abierto para determinar si son iguales.             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Abre una nueva instancia de un proveedor de contenido.                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Indica al proveedor de transporte que imprima un resumen de su estado y cualquier otra información relevante en el registro de seguimiento. |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Recupera los metadatos de una secuencia de contenido abierto.                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Recupera el tamaño de una secuencia de contenido abierto.                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Inicializa un proveedor de contenido.                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Abre una nueva vista estática de una secuencia de contenido.                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Lee el contenido de una secuencia de contenido abierto.                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Indica al proveedor de transporte que debe releer cualquier configuración relevante.                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Shutsdown el proveedor de contenido.                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Especifica el acceso a una secuencia de contenido basándose en el token de un usuario.                                                           |



 

 

 




