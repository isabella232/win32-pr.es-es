---
description: Permite al cliente llamar al objeto de proveedor autocompletar del Panel de entrada de texto de la aplicación.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaz ITipAutocompleteClient (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dac9b1a6c581be8a8fb19df4f812a5866403d949d19739bb8ae99a0fffbe5e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590295"
---
# <a name="itipautocompleteclient-interface"></a>Interfaz ITipAutocompleteClient

Permite al cliente llamar al objeto de proveedor autocompletar del Panel de entrada de texto de la aplicación.

## <a name="members"></a>Miembros

La **interfaz ITipAutocompleteClient** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITipAutocompleteClient** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITipAutocompleteClient** tiene estos métodos.



| Método                                                              | Descripción                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor autocompletar de la aplicación.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Permite al cliente sugerir dónde colocar la lista de autocompletar para evitar que se superponga el Panel de entrada.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina si el Panel de entrada está listo para que se muestra la lista autocompletar.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Anula el registro del proveedor asociado.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Notifica al Panel de entrada que el usuario ha seleccionado algo en la lista autocompletar y que descarta todo el texto restante que aún no se ha insertado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

