---
description: Las \_ constantes LINEINITIALIZEEXOPTION especifican qué mecanismo de notificación de eventos se debe usar al inicializar una sesión.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes de LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690738"
---
# <a name="lineinitializeexoption_-constants"></a>Constantes de LINEINITIALIZEEXOPTION \_

Las **constantes \_ LINEINITIALIZEEXOPTION** especifican qué mecanismo de notificación de eventos se debe usar al inicializar una sesión.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



La aplicación desea utilizar el mecanismo de notificación de eventos de seguimiento del centro de llamadas. Esta constante solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



La aplicación desea utilizar el mecanismo de notificación de eventos del puerto de finalización. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



La aplicación desea utilizar el mecanismo de notificación de eventos de controlador de eventos. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



La aplicación desea utilizar el mecanismo de notificación de eventos de ventana oculta. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Vea [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) para obtener más detalles sobre el funcionamiento de estas opciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




