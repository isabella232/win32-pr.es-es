---
title: Método External.saveCurrentViewToLibrary
description: El método saveCurrentViewToLibrary crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- Método saveCurrentViewToLibrary Reproductor de Windows Media
- Método saveCurrentViewToLibrary Reproductor de Windows Media , Clase externa
- Clase externa Reproductor de Windows Media método saveCurrentViewToLibrary
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
ms.openlocfilehash: cf14a6f712a72116860e7251edae73c91c4ef1dfb70876fd5f80dc329591673a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648445"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>Método External.saveCurrentViewToLibrary

El **método saveCurrentViewToLibrary crea** una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.

## <a name="syntax"></a>Sintaxis


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyListName* \[ En\]
</dt> <dd>

**Cadena** que especifica un nombre descriptivo para la lista de reproducción. Reproductor de Windows Media muestra este nombre en su interfaz de usuario.

</dd> <dt>

*Local* \[ En\]
</dt> <dd>

**Valor** booleano que especifica si la lista de reproducción es dinámica o estática. **TRUE** especifica dynamic y **FALSE,** static.

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

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





