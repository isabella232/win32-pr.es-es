---
title: Estados de los botones de la barra de herramientas (CommCtrl.h)
description: En esta sección se enumeran los estados que puede tener un botón de la barra de herramientas.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166026"
---
# <a name="toolbar-button-states"></a>Estados de los botones de la barra de herramientas

En esta sección se enumeran los estados que puede tener un botón de la barra de herramientas.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ CHECKED**</dt> </dl>                   | El botón tiene el [**estilo TBSTYLE \_ CHECK**](toolbar-control-and-button-styles.md) y se hace clic en el botón.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**PUNTOS \_ SUSPENSIVOS TBSTATE**</dt> </dl>                | [Versión 4.70.](common-control-versions.md) El texto del botón se corta y se muestran los puntos suspensivos.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ ENABLED**</dt> </dl>                   | El botón acepta la entrada del usuario. Un botón que no tiene este estado está atenuado.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ HIDDEN**</dt> </dl>                      | El botón no está visible y no puede recibir la entrada del usuario.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ INDETERMINATE**</dt> </dl> | El botón está atenuado.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ MARCADO**</dt> </dl>                      | [Versión 4.71.](common-control-versions.md) El botón está marcado. La interpretación de un elemento marcado depende de la aplicación. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ PRESSED**</dt> </dl>                   | Se está haciendo clic en el botón.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**TBSTATE \_ WRAP**</dt> </dl>                            | El botón va seguido de un salto de línea. El botón también debe tener el estado TBSTATE \_ ENABLED.<br/>                                              |



## <a name="remarks"></a>Observaciones

Una barra de herramientas puede tener una combinación de estados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





