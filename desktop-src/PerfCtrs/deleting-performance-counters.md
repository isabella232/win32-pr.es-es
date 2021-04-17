---
description: Para quitar los contadores de rendimiento de las aplicaciones del sistema, realice los pasos siguientes.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Eliminar contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667336"
---
# <a name="deleting-performance-counters"></a>Eliminar contadores de rendimiento

Para quitar los contadores de rendimiento de la aplicación del sistema, realice los pasos siguientes.

1.  Utilice la herramienta **Unlodctr** incluida con el equipo para quitar del registro los datos relacionados con los contadores. Tenga en cuenta que la clave de **rendimiento** de la aplicación debe existir para que la herramienta **Unlodctr** se realice correctamente. Para obtener más información, vea [quitar los nombres y descripciones de los contadores del registro](removing-counter-names-and-descriptions-from-the-registry.md).
2.  Elimine las claves de **rendimiento** y **vinculación** en la clave de **servicios** de la aplicación. Para eliminar estas claves, use la utilidad Regedt32.exe o llame a [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
