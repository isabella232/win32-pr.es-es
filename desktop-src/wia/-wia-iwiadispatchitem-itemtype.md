---
description: Tipo de este elemento. Solo lectura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Propiedad Item.ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3cbf60c935a88a62786c7c516ec0e768d65019c02d4419c44d928cee704a67b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450785"
---
# <a name="itemitemtype-property"></a>Propiedad Item.ItemType

Tipo de este elemento. Solo lectura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valor de propiedad

Los valores siguientes son posibles:



| Valor  | Descripción                                     |
|--------|-------------------------------------------------|
| device | El elemento es un dispositivo de hardware WIA.              |
| folder | El elemento es una carpeta que contiene otros elementos. |
| archivo   | El elemento es un archivo de imagen o audio.             |
| audio  | El elemento es un clip de audio.                      |
| imagen  | El elemento es una imagen.                           |



 

## <a name="remarks"></a>Comentarios

Un elemento puede tener más de un tipo. Por ejemplo, cada imagen es de los tipos "image" y "file". **ItemType** devuelve una cadena que incluye todos los tipos válidos para el elemento, separados por punto y coma. Por ejemplo, "image;file". No hay espacios en esta cadena y no hay un punto y coma al final.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




