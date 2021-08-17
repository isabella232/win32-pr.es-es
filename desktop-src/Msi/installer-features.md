---
description: La propiedad Features es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de características publicadas para el producto especificado.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer.Features, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e31dfe2c487a151280a10c4fa7222c005f94c0eeb4ac4f3f5145d67ab600fe9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631477"
---
# <a name="installerfeatures-property"></a>Installer.Features, propiedad

La **propiedad Features** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de características publicadas para el producto especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valor de propiedad

Especifica el código de producto del producto.

## <a name="remarks"></a>Comentarios

Para enumerar las características, una aplicación recorre en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que las características no están ordenadas, cualquier característica nueva tiene un índice arbitrario, lo que significa que la función puede devolver características en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funciones de estado del sistema](installer-function-reference.md)
</dt> </dl>

 

 




