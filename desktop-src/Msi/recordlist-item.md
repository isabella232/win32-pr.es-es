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
ms.openlocfilehash: 7df19a26fd4e8464963f09ffdf227ac88f4376624a88df84d6245efa3c5fd927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041815"
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

## <a name="remarks"></a>Comentarios

El cliente debe comprobar que el [**objeto RecordList**](recordlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad Item.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecordList se define como \_ 000C1096-0000-0000-C000-00000000046<br/>                                                                                                                                                                          |



 

 




