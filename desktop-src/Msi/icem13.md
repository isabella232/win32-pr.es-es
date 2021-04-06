---
description: ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de edición.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909022"
---
# <a name="icem13"></a>ICEM13

ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de edición. La Directiva del publicador y los ensamblados de configuración no deben incluirse en los módulos de combinación destinados a la redistribución, ya que esto puede afectar a otras aplicaciones en el equipo de un usuario.

Este ICEM está disponible en el archivo Mergemod. Cub proporcionado en el SDK de Windows Installer 2,0 y versiones posteriores. Para obtener más información, consulte [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM13 envía un mensaje de ADVERTENCIA Si encuentra un componente especificado en el campo componente de la [tabla MsiAssembly](msiassembly-table.md) del módulo de combinación, que es una directiva de edición o un ensamblado de configuración.

## <a name="example"></a>Ejemplo

ICEM13 envía el siguiente mensaje de ADVERTENCIA Si encuentra una fila en la [tabla MsiAssembly](msiassembly-table.md) con un componente ' \[ 1 \] ' especificado en el campo componente que es una directiva de edición o un ensamblado de configuración que se ha incluido en el módulo de combinación.

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

Es posible instalar la Directiva del publicador y los ensamblados de configuración mediante el Windows Installer, no se recomienda que estos ensamblados se redistribuyan en módulos de combinación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



