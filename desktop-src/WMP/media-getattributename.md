---
title: Método media. getAttributeName
description: El método getAttributeName recupera el nombre del atributo correspondiente al índice especificado.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- método getAttributeName de Windows Media Player
- método getAttributeName Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699442"
---
# <a name="mediagetattributename-method"></a>Método media. getAttributeName

El método **getAttributeName** recupera el nombre del atributo correspondiente al índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que especifica el nombre del atributo.

## <a name="remarks"></a>Observaciones

El nombre de atributo devuelto se puede usar junto con **getItemInfo** para recuperar el valor de un atributo con nombre específico.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **getAttributeName** para rellenar un área de texto HTML denominada mi texto con el índice y el nombre de cada atributo del elemento multimedia actual. El objeto **Player** se creó con ID = "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

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

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





