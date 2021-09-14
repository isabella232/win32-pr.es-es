---
description: La propiedad Item es una propiedad de solo lectura que devuelve un registro en una colección RecordList Object.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Propiedad RecordList.Item
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069710"
---
# <a name="recordlistitem-property"></a>Propiedad RecordList.Item

La **propiedad Item** es una propiedad de solo lectura que devuelve un registro en una colección [**RecordList**](recordlist-object.md) Object.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valor de propiedad

Número de índice del elemento con la colección de cadenas. Se requiere el índice.

## <a name="remarks"></a>Observaciones

El cliente debe comprobar que el [**objeto RecordList**](recordlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad Item.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecordList se define como \_ 000C1096-0000-0000-C000-00000000046<br/>                                                                                                                                                                          |



 

 




