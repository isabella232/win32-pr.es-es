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
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894005"
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

## <a name="remarks"></a>Comentarios

ShortcutTarget devuelve un [**objeto Record**](record-object.md) que contiene tres campos:

-   El campo 1 es un GUID para el código de producto del acceso directo, si está disponible. Este campo puede ser NULL.
-   El campo 2 es el identificador de característica del acceso directo, si está disponible. Este campo puede ser NULL.
-   El campo 3 es un GUID para el código del componente, si está disponible. Este campo puede ser NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




