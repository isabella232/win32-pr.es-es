---
description: Para quitar los contadores de rendimiento de las aplicaciones del sistema, realice los pasos siguientes.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Eliminar contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144018"
---
# <a name="deleting-performance-counters"></a>Eliminar contadores de rendimiento

Para quitar los contadores de rendimiento de la aplicación del sistema, realice los pasos siguientes.

1.  Use la **herramienta unlodctr** incluida con el equipo para quitar los datos relacionados con el contador del registro. Tenga en cuenta que la clave de rendimiento **de** la aplicación debe existir para **que la herramienta unlodctr** se pueda realizar correctamente. Para obtener más información, [vea Quitar nombres y descripciones de contadores del Registro.](removing-counter-names-and-descriptions-from-the-registry.md)
2.  Elimine las **claves Rendimiento** **y Vinculación** en la clave Servicios **de la** aplicación. Para eliminar estas claves, use la utilidad Regedt32.exe o llame [**a RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
