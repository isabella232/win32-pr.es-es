---
title: Servicio de datos remoto quitado
description: Los componentes del servidor de servicio de datos remotos se quitan en Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Servidor RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee18b62bf78bc30aa07cc861963c03baa90c1fd4bc405207b1586ee6167f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935075"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Los componentes del servidor de servicio de datos remotos se quitan en Windows 8

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

El servidor del servicio de datos remoto (RDS) no está disponible en Windows 8:

-   Se quita msadcf.dll archivo, que hospeda el "objeto de negocio" predeterminado RDSServer.DataFactory, y se quitan sus archivos asociados (msadcfr.dll, msadcfr.dll.mui, handler.reg y handsafe.reg).
-   Se msdfmap.dll archivo, que es el controlador predeterminado, y se quita msdfmap.ini archivo.
-   Se msadcs.dll el archivo, isapi,

## <a name="manifestation"></a>Manifestación

Los clientes no pueden hospedar un servidor RDS en Windows 8.

## <a name="mitigation"></a>Mitigación

Los clientes pueden mantener su servidor RDS en una máquina con Windows 7 u otros sistemas operativos de nivel inferior.

## <a name="solution"></a>Solución

Los clientes pueden mantener su servidor RDS en una máquina con Windows 7 u otros sistemas operativos de nivel inferior.

## <a name="resources"></a>Recursos

[Mapa de ruta de las tecnologías de acceso a datos](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 