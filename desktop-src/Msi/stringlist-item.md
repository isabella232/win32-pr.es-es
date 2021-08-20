---
description: La propiedad Item es una propiedad de solo lectura que devuelve una cadena en la colección StringList Object.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Propiedad StringList.Item
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
ms.openlocfilehash: 85962aac5e841c929518a7a37fdada647ce4c74baa69be23048f26f5470c91fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142023"
---
# <a name="stringlistitem-property"></a>Propiedad StringList.Item

La **propiedad Item** es una propiedad de solo lectura que devuelve una cadena en la colección [**StringList Object.**](stringlist-object.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valor de propiedad

Número de índice del elemento con la colección de cadenas. Este parámetro es obligatorio.

## <a name="remarks"></a>Comentarios

El cliente debe comprobar que el [**objeto StringList**](stringlist-object.md) existe y no está vacío antes de hacer referencia a la **propiedad Item.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IStringList se define como \_ 000C1095-0000-0000-C000-00000000046<br/>                                                                                                                                                                          |



 

 




