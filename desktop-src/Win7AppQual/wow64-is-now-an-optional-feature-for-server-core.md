---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Estado de WoW64 en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707290"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 es ahora una característica opcional de Server Core

## <a name="affected-platforms"></a>Plataformas afectadas

**Servidores** : Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto en las características

 **Gravedad** baja  
**Frecuencia** : baja  





## <a name="description"></a>Descripción

La opción de instalación Server Core para Windows Server 2008 R2 le permite desinstalar WoW64. WoW64 es ahora una característica opcional que se puede desinstalar si no es necesario ejecutar código de 32 bits.

Además, los roles Active Directory y Active Directory Lightweight Directory Services requieren WoW64 para ejecutarse en Windows Server 2008 R2.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

Si desinstala WoW64, los administradores que ejecuten código de 32 bits en Server Core recibirán un mensaje de error que indica que la aplicación no se puede ejecutar. Si los administradores intentan ejecutar Active Directory y Active Directory Lightweight Directory Services, recibirán un mensaje de error.

## <a name="mitigation"></a>Mitigación

Instale WoW64.

## <a name="solution"></a>Solución

La solución preferida es proporcionar una versión de 64 bits del código para permitir que se ejecute en Server Core sin necesidad de WoW64.

Como mínimo, proporcione la documentación del usuario que indica que para ejecutar el código de 32 bits, deben instalar WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Compruebe que todo el código usado sea de 64 bits.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Detalles de la implementación de WOW64](../winprog64/wow64-implementation-details.md)
-   [Depurar WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
