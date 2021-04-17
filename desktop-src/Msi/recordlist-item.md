---
description: La propiedad Item es una propiedad de solo lectura que devuelve un registro de una colección de objetos RecordList.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670964"
---
# <a name="recordlistitem-property"></a>RecordList. Item (propiedad)

La propiedad **Item** es una propiedad de solo lectura que devuelve un registro de una colección de objetos [**RecordList**](recordlist-object.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valor de propiedad

Número de índice del elemento con la colección de cadenas. El índice es obligatorio.

## <a name="remarks"></a>Observaciones

El cliente debe comprobar que el objeto [**RecordList**](recordlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad Item.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList se define como 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




