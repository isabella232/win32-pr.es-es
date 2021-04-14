---
description: La propiedad Productosrelacionados de solo lectura devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales con una propiedad UpgradeCode especificada en su tabla de propiedades.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Propiedad Installer. Productosrelacionados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653888"
---
# <a name="installerrelatedproducts-property"></a>Propiedad Installer. Productosrelacionados

La propiedad **productosrelacionados** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales con una propiedad [**UpgradeCode**](upgradecode.md) especificada en su [tabla de propiedades](property-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valor de propiedad

El código de actualización de los productos relacionados enumerados por el instalador.

## <a name="remarks"></a>Observaciones

Para enumerar los productos relacionados, una aplicación recorre en iteración el [**StringList**](stringlist-object.md) con una construcción for each. Dado que los productos relacionados no están ordenados, cualquier nuevo producto relacionado tiene un índice arbitrario. Esto significa que la función puede devolver los productos relacionados en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




