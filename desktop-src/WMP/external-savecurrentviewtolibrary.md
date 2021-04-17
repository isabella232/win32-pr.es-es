---
title: External. saveCurrentViewToLibrary (método)
description: El método saveCurrentViewToLibrary crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- método saveCurrentViewToLibrary de Windows Media Player
- método saveCurrentViewToLibrary de Windows Media Player, clase externa
- Clase externa Windows Media Player, método saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698579"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>External. saveCurrentViewToLibrary (método)

El método **saveCurrentViewToLibrary** crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.

## <a name="syntax"></a>Sintaxis


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyListName* \[ de\]
</dt> <dd>

**Cadena** que especifica un nombre descriptivo para la lista de reproducción. Windows Media Player muestra este nombre en su interfaz de usuario.

</dd> <dt>

*Local* \[ de\]
</dt> <dd>

**Valor booleano** que especifica si la lista de reproducción es dinámica o estática. **True** especifica Dynamic y **false** especifica static.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/>                                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





