---
description: En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funciones de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908093"
---
# <a name="monitor-functions"></a>Funciones de supervisión

En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Crea una instancia del monitor.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Convierte una \_ cadena de versión de CP UTF8 HTML en Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Carga un **valor DWORD** de una cadena de configuración HTML.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Carga una lista de direcciones IP desde una cadena de configuración HTML TEXTAREA.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carga una lista de direcciones IPX desde una cadena de configuración HTML TEXTAREA.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carga una lista de direcciones MAC desde una cadena de configuración HTML TEXTAREA.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transforma una cadena (por ejemplo, "157.54.32.45") en una dirección **DWORD** .                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Busca un nombre de variable solicitado en la cadena de configuración y asigna espacio suficiente (mediante **HeapAllocMemory**) para almacenarlo, copiarlo y devolverlo. |
| [OnLoadingDLL](onloadingdll.md)               | Indica que el archivo DLL comenzó a cargarse. El MCSVC llama a esta función cuando carga por primera vez la DLL del monitor.                                                     |



 

 

 



