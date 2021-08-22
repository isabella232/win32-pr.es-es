---
description: Administra la parte de la aplicación de la integración autocompletar del Panel de entrada de texto.
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
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031873"
---
# <a name="itipautocompleteprovider-interface"></a>Interfaz ITipAutocompleteProvider

Administra la parte de la aplicación de la integración autocompletar del Panel de entrada de texto.

## <a name="members"></a>Miembros

La **interfaz ITipAutocompleteProvider** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteProvider** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITipAutocompleteProvider** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Mostrar**](itipautocompleteprovider-show.md)                           | Muestra u oculta la lista de autocompletar.<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | Lo usa el cliente autocompletar para notificar a la aplicación el texto que un usuario ha escrito en el Panel de entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> <dt>

[**ITipAutocompleteClient (interfaz)**](itipautocompleteclient.md)
</dt> </dl>

 

