---
description: Las constantes LINEINITIALIZEEXOPTION especifican qué mecanismo de notificación de eventos se va \_ a usar al inicializar una sesión.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: LINEINITIALIZEEXOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a1df7c4ea88cad126dcf5b542dbbdc33704814518dbc79cdf5d6bff5da402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073045"
---
# <a name="lineinitializeexoption_-constants"></a>Constantes LINEINITIALIZEEXOPTION \_

Las **constantes LINEINITIALIZEEXOPTION \_** especifican qué mecanismo de notificación de eventos se va a usar al inicializar una sesión.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



La aplicación desea usar el mecanismo de notificación de eventos de seguimiento del centro de llamadas. Esta constante solo se expone a las aplicaciones que negocian una versión TAPI de 3.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



La aplicación desea usar el mecanismo de notificación de eventos puerto de finalización. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



La aplicación desea usar el mecanismo de notificación de eventos event handle. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



La aplicación desea usar el mecanismo de notificación de eventos ventana oculta. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 2.0 o superior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Consulte [**lineInitializeEx para**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) obtener más información sobre el funcionamiento de estas opciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




