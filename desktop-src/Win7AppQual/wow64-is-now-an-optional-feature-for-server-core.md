---
description: WoW64 es ahora una característica opcional para Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Estado de WoW64 en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084053"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 es ahora una característica opcional para Server Core

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores:** Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** baja  
**Frecuencia:** baja  





## <a name="description"></a>Descripción

La opción de instalación Server Core para Windows Server 2008 R2 permite desinstalar WoW64. WoW64 es ahora una característica opcional que se puede desinstalar si no es necesario ejecutar código de 32 bits.

Además, los roles Active Directory y Active Directory Lightweight Directory Services requieren WoW64 para ejecutarse en Windows Server 2008 R2.

## <a name="manifestation-of-impact"></a>Demostración de impacto

Si desinstala WoW64, los administradores que ejecutan código de 32 bits en Server Core recibirán un mensaje de error que indica que no se puede ejecutar la aplicación. Si los administradores intentan ejecutar Active Directory y Active Directory Lightweight Directory Services, recibirán un mensaje de error.

## <a name="mitigation"></a>Mitigación

Instale WoW64.

## <a name="solution"></a>Solución

La solución preferida es proporcionar una versión de 64 bits del código para que se pueda ejecutar en Server Core sin necesidad de WoW64.

Como mínimo, proporcione documentación del usuario que note que para ejecutar código de 32 bits debe instalar WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Compruebe que todo el código usado es de 64 bits.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Detalles de implementación de WOW64](../winprog64/wow64-implementation-details.md)
-   [Depuración de WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
