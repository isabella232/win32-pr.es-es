---
description: La propiedad ShortcutTarget del objeto Installer examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer.ShortcutTarget, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072091"
---
# <a name="installershortcuttarget-property"></a>Installer.ShortcutTarget, propiedad

La **propiedad ShortcutTarget** del objeto [**Installer**](installer-object.md) examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso completa y nombre de archivo para el archivo.

## <a name="remarks"></a>Observaciones

ShortcutTarget devuelve un [**objeto Record**](record-object.md) que contiene tres campos:

-   El campo 1 es un GUID para el código de producto del acceso directo, si está disponible. Este campo puede ser NULL.
-   El campo 2 es el identificador de característica del acceso directo, si está disponible. Este campo puede ser NULL.
-   El campo 3 es un GUID para el código del componente, si está disponible. Este campo puede ser NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




