---
title: Funciones del proveedor de transporte wds
description: Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1044c923226dcc618e816219dcec9d7edf78855e03acf13b76ba4d7ed9ad15a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053263"
---
# <a name="wds-transport-provider-functions"></a>Funciones del proveedor de transporte wds

Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.



| Función                                                                               | Descripción                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Cierra un flujo de contenido especificado por un identificador.                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Cierra una instancia de un proveedor de contenido especificado por un identificador.                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Compara un nombre de contenido y una instancia especificados con un flujo de contenido abierto para determinar si son iguales.             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Abre una nueva instancia de un proveedor de contenido.                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Indica al proveedor de transporte que imprima un resumen de su estado y cualquier otra información pertinente en el registro de seguimiento. |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Recupera los metadatos de un flujo de contenido abierto.                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Recupera el tamaño de un flujo de contenido abierto.                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Inicializa un proveedor de contenido.                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Abre una nueva vista estática de una secuencia de contenido.                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Lee contenido de una secuencia de contenido abierta.                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Indica al proveedor de transporte que vuelva a leer cualquier configuración pertinente.                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Cierra el proveedor de contenido.                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Especifica el acceso a un flujo de contenido basado en el token de un usuario.                                                           |



 

 

 




