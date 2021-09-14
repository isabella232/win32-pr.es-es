---
description: Con el tiempo, pueden existir versiones diferentes para las aplicaciones TAPI, TAPI y los proveedores de servicios.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negociación de las versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068699"
---
# <a name="version-negotiation"></a>Negociación de las versiones

Con el tiempo, pueden existir versiones diferentes para las aplicaciones TAPI, TAPI y los proveedores de servicios. La interoperabilidad óptima de una aplicación TAPI requiere el conocimiento no solo de la versión de TAPI de la aplicación, sino también de las versiones del proveedor de servicios, TAPISVR y DLL de TAPI.

Si no se hace correctamente la negociación de versiones, se pueden producir problemas graves. Por ejemplo, algunas estructuras muy usadas tienen miembros de datos agregados de una versión a la siguiente. Si el tamaño de la estructura no coincide con lo que espera la aplicación o TAPI, las consecuencias van desde pérdidas de memoria hasta AVs intermitentes.

Para obtener información adicional, vea [Control de versiones de TAPI.](./tapi-versioning.md)

**TAPI 2.x:** Las aplicaciones negocian con TAPI y TAPISVR durante [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Las aplicaciones realizan la negociación de dispositivos con proveedores de servicios mediante una llamada [**a lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) para cada línea que la aplicación pueda usar.

**TAPI 3.x:** No es necesario realizar la negociación de versiones; sin embargo, puede usar [**QueryInterface para**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) determinar si una interfaz está disponible en su versión.

 

 
