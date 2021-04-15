---
description: Administra una operación de suspensión de aplicación retrasada.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interfaz ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648192"
---
# <a name="isuspendingdeferral-interface"></a>Interfaz ISuspendingDeferral

Administra una operación de suspensión de aplicación retrasada.

## <a name="members"></a>Miembros

La interfaz **ISuspendingDeferral** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingDeferral** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISuspendingDeferral** tiene estos métodos.



| Método                                           | Descripción                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Completo**](isuspendingdeferral-complete.md) | Notifica al sistema que la aplicación ha guardado sus datos y está listo para su suspensión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Encabezado<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
