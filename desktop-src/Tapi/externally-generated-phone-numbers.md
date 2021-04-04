---
description: Un proveedor de servicios puede indicar números de teléfono generados externamente mediante la configuración de miembros de la estructura LINECALLINFO al procesar la \_ función TSPI lineGetCallInfo.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Números de teléfono generados externamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809860"
---
# <a name="externally-generated-phone-numbers"></a>Números de teléfono generados externamente

Un proveedor de servicios puede indicar números de teléfono generados externamente (es decir, números de llamadas salientes que se generan externamente en el equipo) mediante el establecimiento de los miembros **DisplayableAddress**, **CalledParty** o [comment](./comment-ovr.md) en la estructura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) al procesar la función [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) . Si TAPI no ha guardado sus propios datos para estos miembros, deja sin modificar los datos establecidos por el proveedor de servicios. Si TAPI tiene datos almacenados en caché para estos miembros, TAPI agrega su texto al final de la parte variable de la estructura **LINECALLINFO** y sobrescribe el tamaño y el desplazamiento que el proveedor de servicios ha colocado en la parte fija.

Un proveedor de servicios también puede copiar un número de salida en el miembro **CalledID** . Por lo tanto, las aplicaciones de registro deben comprobar el miembro **CalledID** en las llamadas salientes si los miembros **DisplayableAddress** y **CalledParty** están vacíos.

 

 
