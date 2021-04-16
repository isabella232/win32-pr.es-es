---
title: Estados del botón de la barra de herramientas (CommCtrl. h)
description: En esta sección se enumeran los Estados que puede tener un botón de la barra de herramientas.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649769"
---
# <a name="toolbar-button-states"></a>Estados del botón de la barra de herramientas

En esta sección se enumeran los Estados que puede tener un botón de la barra de herramientas.



| Constante                                                                                                                                                                              | Descripción                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ activado**</dt> </dl>                   | El botón tiene el estilo de [**\_ comprobación TBSTYLE**](toolbar-control-and-button-styles.md) y se está haciendo clic en él.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**TBSTATE \_ puntos suspensivos**</dt> </dl>                | [Versión 4,70](common-control-versions.md). El texto del botón se corta y se muestran puntos suspensivos.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ habilitado**</dt> </dl>                   | El botón acepta los datos proporcionados por el usuario. Un botón que no tiene este estado está atenuado.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ oculto**</dt> </dl>                      | El botón no está visible y no puede recibir datos proporcionados por el usuario.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ indeterminado**</dt> </dl> | El botón está atenuado.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ marcados**</dt> </dl>                      | [Versión 4,71](common-control-versions.md). El botón está marcado como. La interpretación de un elemento marcado depende de la aplicación. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ presionado**</dt> </dl>                   | Se está haciendo clic en el botón.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**TBSTATE \_ Wrap**</dt> </dl>                            | El botón va seguido de un salto de línea. El botón también debe tener el \_ estado habilitado de TBSTATE.<br/>                                              |



## <a name="remarks"></a>Observaciones

Una barra de herramientas puede tener una combinación de Estados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





