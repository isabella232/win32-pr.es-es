---
description: La propiedad Instalado solo se establece si el producto está instalado por equipo o para el usuario actual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propiedad instalada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171766"
---
# <a name="installed-property"></a>Propiedad instalada

La **propiedad Instalado** solo se establece si el producto está instalado por equipo o para el usuario actual. Esta propiedad no se establece si el producto está instalado para otro usuario.

La **propiedad Instalado** se puede usar en expresiones condicionales para determinar si un producto está instalado por equipo o para el usuario actual. Por ejemplo, la propiedad se puede usar en la columna condicional de una tabla de secuencia o para diferenciar entre una primera instalación y una instalación de mantenimiento.

Para determinar si el producto está instalado para otro usuario, compruebe la [**propiedad ProductState.**](productstate.md)

El valor de la [**propiedad ProductVersion**](productversion.md) es la versión del producto en formato de cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




