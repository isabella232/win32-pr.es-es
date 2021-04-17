---
description: La propiedad Products es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Propiedad Installer. Products
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653639"
---
# <a name="installerproducts-property"></a>Propiedad Installer. Products

La propiedad **Products** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para enumerar los productos, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each. Dado que los productos no están ordenados, cualquier producto nuevo tiene un índice arbitrario. Esto significa que la función puede devolver los productos en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




