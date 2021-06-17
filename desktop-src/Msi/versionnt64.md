---
description: El instalador establece la propiedad VersionNT64 en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propiedad VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262077"
---
# <a name="versionnt64-property"></a>Propiedad VersionNT64

El instalador establece la **propiedad VersionNT64** en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits. La propiedad no está definida si el sistema operativo no es de 64 bits.

El valor es un entero: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidad, la propiedad [](template-summary.md) tampoco está definida si la propiedad Resumen de plantilla indica que el paquete es para sistemas Intel (x86) de 32 bits y el sistema operativo no puede ejecutar código Intel (x64) de 64 bits, como Windows 10 en ARM (ARM64).

> [!NOTE]
> A partir Windows 10 compilación 21277, las compilaciones de ARM64 en el canal de desarrollo del programa Windows Insider Preview admiten aplicaciones x64. En estas compilaciones arm64, la propiedad VersionNT64 se define para los paquetes x86.

## <a name="remarks"></a>Observaciones

Las expresiones condicionales prueban Windows de 64 bits simplemente con el nombre de propiedad o comprobando la versión mediante un operador de comparación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP Consulte los requisitos de [Windows Installer Run-Time](windows-installer-portal.md) para obtener información sobre el Service Pack de Windows mínimo que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




