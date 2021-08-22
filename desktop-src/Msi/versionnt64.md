---
description: El instalador establece la propiedad VersionNT64 en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285f97a6325df65ace9ff6620489697e6eeeb573761437bd0a826dec4dc31e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526935"
---
# <a name="versionnt64-property"></a>VersionNT64, propiedad

El instalador establece la **propiedad VersionNT64** en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits. La propiedad no está definida si el sistema operativo no es de 64 bits.

El valor es un entero: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidad, la propiedad [](template-summary.md) tampoco está definida si la propiedad Resumen de plantilla indica que el paquete es para sistemas Intel (x86) de 32 bits y el sistema operativo no puede ejecutar código Intel (x64) de 64 bits, como Windows 10 en ARM (ARM64).

> [!NOTE]
> A partir Windows 10 compilación 21277, las compilaciones de ARM64 en el canal de desarrollo del programa Windows Insider Preview admiten aplicaciones x64. En estas compilaciones arm64, la propiedad VersionNT64 se define para los paquetes x86.

## <a name="remarks"></a>Comentarios

Las expresiones condicionales prueban los Windows de 64 bits simplemente con el nombre de propiedad o comprobando la versión mediante un operador de comparación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP Consulte los requisitos de Run-Time del instalador de [Windows](windows-installer-portal.md) para obtener información sobre el service pack de Windows mínimo que requiere una versión del instalador de Windows.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




