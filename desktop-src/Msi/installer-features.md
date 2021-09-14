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
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171661"
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

## <a name="remarks"></a>Observaciones

Para enumerar las características, una aplicación recorre en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que las características no están ordenadas, cualquier característica nueva tiene un índice arbitrario, lo que significa que la función puede devolver características en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




