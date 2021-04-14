---
description: La propiedad patches de solo lectura del objeto Installer devuelve un objeto StringList que contiene todas las revisiones aplicadas al producto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Propiedad Installer. patches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653897"
---
# <a name="installerpatches-property"></a>Propiedad Installer. patches

La propiedad **patches** de solo lectura del objeto [**Installer**](installer-object.md) devuelve un objeto [**StringList**](stringlist-object.md) que contiene todas las revisiones aplicadas al producto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valor de propiedad

Especifica el código de producto.

## <a name="remarks"></a>Observaciones

Para enumerar las revisiones, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) con una construcción for each. Dado que las revisiones no están ordenadas, las nuevas revisiones tienen un índice arbitrario. Esto significa que la función puede devolver revisiones en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




