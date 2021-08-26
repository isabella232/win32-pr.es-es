---
description: La propiedad UILevel del objeto Installer es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores dentro del espacio de proceso actual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer.UILevel, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3004675ee8e07c3503ec4442832c00975364066fa4a0c770b0b081fc7b64c3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043575"
---
# <a name="installeruilevel-property"></a>Installer.UILevel, propiedad

La **propiedad UILevel** del objeto [**Installer**](installer-object.md) es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores dentro del espacio de proceso actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios



| Nivel de interfaz de usuario   | Value | Descripción                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | No cambia el nivel de la interfaz de usuario.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Usa el nivel de interfaz de usuario predeterminado.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Instalación silenciosa.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Progreso sencillo y control de errores.                                                                                                                                                                |
| msiUILevelReduced      | 4     | Se han suprimido los cuadros de diálogo de interfaz de usuario y asistentes.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interfaz de usuario de creación con asistentes, progreso y errores.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Si se combina con el valor msiUILevelBasic, el instalador  muestra cuadros de diálogo de progreso, pero no muestra un botón Cancelar en el cuadro de diálogo para impedir que los usuarios cancelen la instalación. |
| msiUILevelProgressOnly | 64    | Si se combina con el valor msiUILevelBasic, el instalador muestra cuadros de diálogo de progreso, pero no muestra cuadros de diálogo modales ni cuadros de diálogo de error.                                        |
| msiUILevelEndDialog    | 128   | Si se combina con cualquier valor anterior, el instalador muestra un cuadro de diálogo modal al final de una instalación correcta o si se ha producido un error. No se muestra ningún cuadro de diálogo si el usuario cancela. |



 

Vea también Determinar [el nivel de la interfaz de usuario a partir de una acción personalizada.](determining-ui-level-from-a-custom-action.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




