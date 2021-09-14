---
description: La propiedad Products es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Installer.Products, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072113"
---
# <a name="installerproducts-property"></a>Installer.Products, propiedad

La **propiedad Products** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para enumerar los productos, una aplicación recorre en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que los productos no están ordenados, cualquier producto nuevo tiene un índice arbitrario. Esto significa que la función puede devolver productos en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




