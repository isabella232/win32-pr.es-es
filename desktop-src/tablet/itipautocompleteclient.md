---
description: Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaz ITipAutocompleteClient (TipAutoComplete. h)
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
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717069"
---
# <a name="itipautocompleteclient-interface"></a>Interfaz ITipAutocompleteClient

Permite al cliente llamar al objeto de proveedor de finalización automática del panel de entrada de texto de la aplicación.

## <a name="members"></a>Miembros

La interfaz **ITipAutocompleteClient** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITipAutocompleteClient** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITipAutocompleteClient** tiene estos métodos.



| Método                                                              | Descripción                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | Permite al cliente sugerir dónde colocar la lista de Autocompletar para evitar la superposición del panel de entrada.<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | Determina si el panel de entrada está listo para mostrar la lista de autocompletar.<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | Anula el registro del proveedor asociado.<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

