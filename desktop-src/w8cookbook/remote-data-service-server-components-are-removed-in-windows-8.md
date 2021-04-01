---
title: Servicio de datos remotos quitado
description: Los componentes del servidor de servicio de datos remotos se quitan en Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Servidor RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103995697"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>Los componentes del servidor de servicio de datos remotos se quitan en Windows 8

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  



## <a name="description"></a>Descripción

El servidor del servicio de datos remoto (RDS) no está disponible en Windows 8:

-   Se quita el msadcf.dll de archivos, que hospeda el "objeto comercial" predeterminado RDSServer. DataFactory, y se quitan los archivos asociados (msadcfr.dll, msadcfr.dll. MUI, handler. reg y Handsafe. reg)
-   msdfmap.dll de archivo, que es el controlador predeterminado, se quita y se quita el archivo msdfmap.ini
-   msadcs.dll de archivo, ISAPI, se quita

## <a name="manifestation"></a>Manifestación

Los clientes no pueden hospedar un servidor RDS en Windows 8.

## <a name="mitigation"></a>Mitigación

Los clientes pueden mantener su servidor RDS en un equipo con Windows 7 u otros sistemas operativos de nivel inferior.

## <a name="solution"></a>Solución

Los clientes pueden mantener su servidor RDS en un equipo con Windows 7 u otros sistemas operativos de nivel inferior.

## <a name="resources"></a>Recursos

[Mapa de ruta de las tecnologías de acceso a datos](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 