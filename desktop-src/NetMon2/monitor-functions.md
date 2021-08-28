---
description: En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Funciones de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677105"
---
# <a name="monitor-functions"></a>Funciones de supervisión

En esta sección se describen las funciones auxiliares que puede usar para desarrollar monitores personalizados.



| Función                                       | Descripción                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Crea una instancia del monitor.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Convierte una cadena de versión UTF8 de HTML CP \_ en Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Carga un **DWORD desde** una cadena de configuración HTML.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Carga una lista de direcciones IP desde una cadena de configuración TEXTAREA HTML.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Carga una lista de direcciones IPX desde una cadena de configuración TEXTAREA HTML.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Carga una lista de direcciones MAC desde una cadena de configuración TEXTAREA HTML.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transforma una cadena (como "157.54.32.45") en una **dirección DWORD.**                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Busca un nombre de variable solicitado en la cadena de configuración y asigna espacio suficiente (mediante **HeapAllocMemory)** para almacenarlo, copiarlo y devolverlo. |
| [OnLoadingDLL](onloadingdll.md)               | Indica que el archivo DLL ha empezado a cargarse. MCSVC llama a esta función cuando carga por primera vez el archivo DLL del monitor.                                                     |



 

 

 



