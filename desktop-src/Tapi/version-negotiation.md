---
description: Con el tiempo, pueden existir diferentes versiones para las aplicaciones TAPI, TAPI y los proveedores de servicios.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negociación de las versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002748"
---
# <a name="version-negotiation"></a>Negociación de las versiones

Con el tiempo, pueden existir diferentes versiones para las aplicaciones TAPI, TAPI y los proveedores de servicios. La interoperabilidad óptima de una aplicación TAPI requiere conocimiento de no solo la versión de TAPI de la aplicación, sino también de la DLL de TAPI, TAPISVR y las versiones del proveedor de servicios.

Si no se realiza la negociación de la versión correcta, pueden producirse problemas graves. Por ejemplo, algunas estructuras de uso intensivo tienen miembros de datos agregados de una versión a la siguiente. Si el tamaño de la estructura no coincide con lo que la aplicación o TAPI espera, las consecuencias van desde pérdidas de memoria hasta AVs intermitente.

Para obtener más información, consulte [control de versiones de TAPI](./tapi-versioning.md).

**TAPI 2. x:** Las aplicaciones negocian con TAPI y TAPISVR durante [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Las aplicaciones realizan la negociación de dispositivos con proveedores de servicios mediante una llamada a [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) para cada línea que pueda usar la aplicación.

**TAPI 3. x:** No es necesario realizar la negociación de la versión; sin embargo, puede usar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para determinar si una interfaz está disponible en su versión.

 

 
