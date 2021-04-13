---
description: Proporciona datos para un evento de suspensión de la aplicación.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interfaz ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648191"
---
# <a name="isuspendingeventargs-interface"></a>Interfaz ISuspendingEventArgs

Proporciona datos para un evento de suspensión de la aplicación.

## <a name="members"></a>Miembros

La interfaz **ISuspendingEventArgs** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingEventArgs** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **ISuspendingEventArgs** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Lectura/escritura<br/> | Obtiene la operación de suspensión de la aplicación.<br/> |



 

## <a name="remarks"></a>Observaciones

Se tiene acceso a este objeto cuando se implementan controladores de eventos como [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)y se produce la [**\_ suspensión**](/previous-versions//hh438376(v=vs.85)) para responder a eventos de suspensión de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Encabezado<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
