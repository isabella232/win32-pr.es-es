---
title: Media.attributeCount
description: La propiedad attributeCount recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media.attributeCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967507"
---
# <a name="mediaattributecount"></a>Media.attributeCount

La **propiedad attributeCount** recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.

## <a name="syntax"></a>Sintaxis

*player*. *currentMedia*. **attributeCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

**Reproductor de Windows Media 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **attributeCount** para determinar el número de atributos disponibles en el elemento multimedia actual. El código usa ese valor para imprimir una lista de nombres y valores de atributo en un área de texto HTML, denominada myText. El **objeto Player** se creó con id. = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





