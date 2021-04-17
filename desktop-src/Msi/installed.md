---
description: La propiedad installed solo se establece si el producto se instala por equipo o para el usuario actual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propiedad installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653790"
---
# <a name="installed-property"></a>Propiedad installed

La propiedad **installed** solo se establece si el producto se instala por equipo o para el usuario actual. Esta propiedad no se establece si el producto está instalado para un usuario diferente.

La propiedad **installed** se puede usar en expresiones condicionales para determinar si un producto está instalado por equipo o para el usuario actual. Por ejemplo, la propiedad se puede utilizar en la columna condicional de una tabla de secuencia o para diferenciar entre una instalación de primera instalación y otra de mantenimiento.

Para determinar si el producto está instalado para un usuario diferente, Compruebe la propiedad [**ProductState**](productstate.md) .

El valor de la propiedad [**ProductVersion**](productversion.md) es la versión del producto en formato de cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




