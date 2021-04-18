---
description: Tipo de este elemento. Solo lectura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Propiedad Item. ItemType
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
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720534"
---
# <a name="itemitemtype-property"></a>Propiedad Item. ItemType

Tipo de este elemento. Solo lectura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Valor de propiedad

Los valores siguientes son posibles:



| Value  | Descripción                                     |
|--------|-------------------------------------------------|
| device | El elemento es un dispositivo de hardware WIA.              |
| folder | El elemento es una carpeta que contiene otros elementos. |
| archivo   | El elemento es un archivo de imagen o de audio.             |
| audio  | El elemento es un clip de audio.                      |
| imagen  | El elemento es una imagen.                           |



 

## <a name="remarks"></a>Observaciones

Un elemento puede tener más de un tipo. Por ejemplo, cada imagen tiene los tipos "imagen" y "archivo". **ItemType** devuelve una cadena que incluye todos los tipos válidos para el elemento, separados por punto y coma. Por ejemplo, "Image; File". No hay espacios en esta cadena y no hay un punto y coma al final.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




