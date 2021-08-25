---
description: ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de publicador.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678b89e14cb699bb6207be5c2e14473de2a743494b47ff5ae5e0ccda2a9cc9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894285"
---
# <a name="icem13"></a>ICEM13

ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de publicador. Publisher ensamblados de configuración y directiva no deben incluirse en módulos de combinación destinados a la redistribución, ya que esto puede afectar a otras aplicaciones en el equipo de un usuario.

Este ICEM está disponible en el archivo Mergemod.uu proporcionado en el SDK Windows Installer 2.0 y versiones posteriores. Para obtener más información, [consulte Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM13 envía un mensaje de advertencia si encuentra un componente especificado en el campo Componente de la tabla [MsiAssembly](msiassembly-table.md) del módulo de mezcla que es una directiva de publicador o un ensamblado de configuración.

## <a name="example"></a>Ejemplo

ICEM13 publica el siguiente mensaje de advertencia si encuentra una fila en la tabla [MsiAssembly](msiassembly-table.md) con un componente '1' especificado en el campo Componente que es una directiva de publicador o un ensamblado de configuración que se ha incluido en el módulo de \[ \] combinación.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

Es posible instalar ensamblados de configuración y directivas de publicador mediante el instalador de Windows, no se recomienda redistribuir estos ensamblados en módulos de combinación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



