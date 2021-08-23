---
title: Media.name
description: La propiedad name especifica o recupera el nombre del elemento multimedia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616861"
---
# <a name="medianame"></a>Media.name

La **propiedad** name especifica o recupera el nombre del elemento multimedia.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **name**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de **lectura** y escritura que contiene el nombre del elemento multimedia.

## <a name="remarks"></a>Comentarios

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para especificar el valor de esta propiedad, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Antes de usar este método para especificar el nombre de un elemento multimedia, use **isReadOnlyItem para** determinar si se puede establecer el nombre.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad es de solo lectura.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **name** para cambiar el nombre del elemento multimedia actual. Un elemento de entrada HTML TEXT denominado NameText permite al usuario escribir una cadena de texto para el nuevo nombre. El **objeto Player** se creó con id. = "Player".


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





