---
description: Si esta directiva del sistema por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074403"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Si esta directiva [](system-policy.md) del sistema por equipo se establece en un valor mayor que 0, Windows Installer guarda las versiones anteriores de los archivos en una memoria caché cuando se aplica una revisión a una aplicación. El almacenamiento en caché puede aumentar el rendimiento de las instalaciones futuras que, de lo contrario, necesitan obtener los archivos antiguos de un origen de aplicación original.

El valor de la directiva MaxPatchCacheSize es el porcentaje máximo de espacio en disco que el instalador puede usar para la memoria caché de archivos antiguos. Por ejemplo, un valor de 20 especifica que no se usará más del 20 %. Si el tamaño total de la memoria caché alcanza el porcentaje especificado de espacio en disco, no se guardan archivos adicionales en la memoria caché. La directiva no afecta a los archivos que ya se han guardado.

Si el valor de la directiva MaxPatchCacheSize está establecido en 0, no se guardan archivos adicionales.

Si no se establece la directiva MaxPatchCacheSize, el valor predeterminado es 10 y se puede usar un máximo del 10 % del espacio en disco para guardar archivos antiguos.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



