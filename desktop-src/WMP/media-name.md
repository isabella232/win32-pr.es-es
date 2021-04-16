---
title: Media.name
description: La propiedad Name especifica o recupera el nombre del elemento multimedia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
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
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699814"
---
# <a name="medianame"></a>Media.name

La propiedad **Name** especifica o recupera el nombre del elemento multimedia.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. **nombre** de

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura que contiene el nombre del elemento multimedia.

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para especificar el valor de esta propiedad, se requiere acceso total a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Antes de utilizar este método para especificar el nombre de un elemento multimedia, use **isReadOnlyItem** para determinar si se puede establecer el nombre.

**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **nombre** para cambiar el nombre del elemento multimedia actual. Un elemento de entrada de texto HTML denominado NameText permite al usuario escribir una cadena de texto para el nuevo nombre. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





