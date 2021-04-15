---
description: Si esta Directiva del sistema por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497699"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Si esta [Directiva del sistema](system-policy.md) por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación. El almacenamiento en caché puede aumentar el rendimiento de las instalaciones futuras que, de otro modo, necesitan obtener los archivos antiguos de un origen de aplicación original.

El valor de la Directiva MaxPatchCacheSize es el porcentaje máximo de espacio en disco que puede usar el instalador para la caché de archivos antiguos. Por ejemplo, un valor de 20 no especifica más del 20%. Si el tamaño total de la memoria caché alcanza el porcentaje especificado de espacio en disco, no se guarda ningún archivo adicional en la memoria caché. La Directiva no afecta a los archivos que ya se han guardado.

Si el valor de la Directiva MaxPatchCacheSize se establece en 0, no se guarda ningún archivo adicional.

Si no se establece la Directiva MaxPatchCacheSize, el valor predeterminado es 10 y se puede usar un máximo del 10% del espacio en disco para guardar los archivos antiguos.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



