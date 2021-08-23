---
description: La propiedad Patches de solo lectura del objeto Installer devuelve un objeto StringList que contiene todas las revisiones aplicadas al producto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer.Patches, propiedad
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
ms.openlocfilehash: 33576b92924493a99c058196639faa34f5b42e388b9e30b6e300c17444ddeeff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430785"
---
# <a name="installerpatches-property"></a>Installer.Patches, propiedad

La propiedad **Patches de** solo lectura del objeto [**Installer**](installer-object.md) devuelve un [**objeto StringList**](stringlist-object.md) que contiene todas las revisiones aplicadas al producto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valor de propiedad

Especifica el código de producto.

## <a name="remarks"></a>Comentarios

Para enumerar las revisiones, una aplicación recorre en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que las revisiones no están ordenadas, cualquier nueva revisión tiene un índice arbitrario. Esto significa que la función puede devolver revisiones en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




