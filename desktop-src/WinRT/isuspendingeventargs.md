---
description: Proporciona datos para un evento de suspensión de aplicaciones.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interfaz ISuspendingEventArgs (Windows. ApplicationModel.h)
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
ms.openlocfilehash: 6b8eb9f4a93aafd52f53bc6caabf74c7855f8b835d680dd53e87bd71ea28ad67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993785"
---
# <a name="isuspendingeventargs-interface"></a>Interfaz ISuspendingEventArgs

Proporciona datos para un evento de suspensión de aplicaciones.

## <a name="members"></a>Miembros

La **interfaz ISuspendingEventArgs** hereda de [**IInspectable.**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) **ISuspendingEventArgs** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz ISuspendingEventArgs** tiene estas propiedades.



| Propiedad                                                                           | Tipo de acceso           | Descripción                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Lectura/escritura<br/> | Obtiene la operación de suspensión de la aplicación.<br/> |



 

## <a name="remarks"></a>Comentarios

Se tiene acceso a este objeto cuando se implementan controladores de eventos como [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)y se agrega [**\_ Suspending**](/previous-versions//hh438376(v=vs.85)) para responder a eventos de suspensión de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
