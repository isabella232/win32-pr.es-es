---
description: El instalador establece la propiedad VersionNT64 en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propiedad VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679411"
---
# <a name="versionnt64-property"></a>Propiedad VersionNT64

El instalador establece la propiedad **VersionNT64** en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits. Si el sistema operativo no es de 64 bits, la propiedad no está definida.

El valor es un entero: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidad, la propiedad también está sin definir si la propiedad de Resumen de la [**plantilla**](template-summary.md) indica que el paquete es para los sistemas Intel de 32 bits y el sistema operativo es una arquitectura de 64 bits que no es Intel64 ni x64 (como ARM64).

## <a name="remarks"></a>Observaciones

Las expresiones condicionales prueban para Windows de 64 bits simplemente con el nombre de propiedad, o bien comprobando la versión con un operador de comparación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP, consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows necesaria para una versión de Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




