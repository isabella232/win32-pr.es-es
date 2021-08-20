---
description: La propiedad RelatedProducts de solo lectura devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales con una propiedad UpgradeCode especificada en su tabla Property.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer.RelatedProducts, propiedad
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
ms.openlocfilehash: 15e84a063b8f094dbeee02f3000bdd1c69356f5fa664f6e6f6aff87d19d07dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946143"
---
# <a name="installerrelatedproducts-property"></a>Installer.RelatedProducts, propiedad

La propiedad **RelatedProducts** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales con una propiedad [**UpgradeCode**](upgradecode.md) especificada en su tabla [Property](property-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>Valor de propiedad

Código de actualización de productos relacionados que enumera el instalador.

## <a name="remarks"></a>Comentarios

Para enumerar los productos relacionados, una aplicación recorre en iteración [**stringlist**](stringlist-object.md) mediante una construcción For Each. Dado que los productos relacionados no están ordenados, cualquier nuevo producto relacionado tiene un índice arbitrario. Esto significa que la función puede devolver productos relacionados en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




