---
description: El AdminProperties debe crearse en la tabla de propiedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propiedad AdminProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671795"
---
# <a name="adminproperties-property"></a>Propiedad AdminProperties

El **AdminProperties** debe crearse en la [tabla de propiedades](property-table.md). El valor de **AdminProperties** es una lista de nombres de propiedad separados por signos de punto y coma. El instalador guarda los valores de estas propiedades enumeradas en el momento de una [instalación administrativa](administrative-installation.md). Cuando los usuarios instalan desde la imagen administrativa, la instalación usa los valores guardados de las propiedades, en lugar de los valores del archivo. msi.

## <a name="remarks"></a>Observaciones

Los nombres de propiedad de la lista pueden ser letras mayúsculas y minúsculas (propiedades privadas) o todas mayúsculas (propiedades públicas).

Esta propiedad nunca debe terminar con un punto y coma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




