---
description: La propiedad Features es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de características publicadas para el producto especificado.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Propiedad Installer. Features
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653348"
---
# <a name="installerfeatures-property"></a>Propiedad Installer. Features

La propiedad **Features** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de características publicadas para el producto especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valor de propiedad

Especifica el código de producto del producto.

## <a name="remarks"></a>Observaciones

Para enumerar las características, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each. Dado que las características no están ordenadas, todas las características nuevas tienen un índice arbitrario, lo que significa que la función puede devolver características en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funciones de estado del sistema](installer-function-reference.md)
</dt> </dl>

 

 




