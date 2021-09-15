---
description: Administra la parte de la aplicación de la integración de autocompletar del Panel de entrada de texto.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interfaz ITipAutocompleteProvider (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579424"
---
# <a name="itipautocompleteprovider-interface"></a>Interfaz ITipAutocompleteProvider

Administra la parte de la aplicación de la integración de autocompletar del Panel de entrada de texto.

## <a name="members"></a>Members

La **interfaz ITipAutocompleteProvider** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITipAutocompleteProvider** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Mostrar**](itipautocompleteprovider-show.md)                           | Muestra u oculta la lista de autocompletar.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Lo usa el cliente de autocompletar para notificar a la aplicación el texto que un usuario ha escrito en el Panel de entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> <dt>

[**ITipAutocompleteClient (interfaz)**](itipautocompleteclient.md)
</dt> </dl>

 

