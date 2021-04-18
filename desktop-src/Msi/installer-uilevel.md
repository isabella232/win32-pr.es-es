---
description: La propiedad elemento uilevel del objeto de instalador es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores en el espacio de proceso actual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Propiedad Installer. elemento uilevel
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
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653992"
---
# <a name="installeruilevel-property"></a>Propiedad Installer. elemento uilevel

La propiedad **elemento uilevel** del objeto de [**instalador**](installer-object.md) es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores en el espacio de proceso actual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones



| Nivel de interfaz de usuario   | Value | Descripción                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | No cambia el nivel de la interfaz de usuario.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Usa el nivel de IU predeterminado.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Instalación silenciosa.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Progreso simple y control de errores.                                                                                                                                                                |
| msiUILevelReduced      | 4     | La interfaz de usuario creada y los cuadros de diálogo del asistente se han suprimido.                                                                                                                                                    |
| msiUILevelFull         | 5     | Interfaz de usuario creada con asistentes, progreso y errores.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | Si se combina con el valor msiUILevelBasic, el instalador muestra cuadros de diálogo de progreso pero no muestra un botón **Cancelar** en el cuadro de diálogo para impedir que los usuarios cancelen la instalación. |
| msiUILevelProgressOnly | 64    | Si se combina con el valor msiUILevelBasic, el instalador muestra cuadros de diálogo de progreso pero no muestra cuadros de diálogo modales ni cuadros de diálogo de error.                                        |
| msiUILevelEndDialog    | 128   | Si se combina con cualquier valor anterior, el instalador muestra un cuadro de diálogo modal al final de una instalación correcta o si se ha producido un error. No se muestra ningún cuadro de diálogo si el usuario cancela. |



 

Vea también [determinar el nivel de interfaz de usuario desde una acción personalizada](determining-ui-level-from-a-custom-action.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




