---
description: La propiedad Item es una propiedad de solo lectura que devuelve una cadena en la colección de objetos StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653833"
---
# <a name="stringlistitem-property"></a>StringList. Item (propiedad)

La propiedad **Item** es una propiedad de solo lectura que devuelve una cadena en la colección de [**objetos StringList**](stringlist-object.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valor de propiedad

Número de índice del elemento con la colección de cadenas. Este parámetro es necesario.

## <a name="remarks"></a>Observaciones

El cliente debe comprobar que el [**objeto StringList**](stringlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad **Item** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IStringList se define como 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




