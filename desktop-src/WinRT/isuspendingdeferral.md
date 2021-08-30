---
description: Administra una operación de suspensión de aplicaciones retrasada.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interfaz ISuspendingDeferral (Windows. ApplicationModel.h)
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
ms.openlocfilehash: 16a9d61dc68d296d39ab5a76b634d136a8e88b8987ac4990696a43ab396b68e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898665"
---
# <a name="isuspendingdeferral-interface"></a>Interfaz ISuspendingDeferral

Administra una operación de suspensión de aplicaciones retrasada.

## <a name="members"></a>Miembros

La **interfaz ISuspendingDeferral** hereda de [**IInspectable.**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) **ISuspendingDeferral** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISuspendingDeferral** tiene estos métodos.



| Método                                           | Descripción                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Completo**](isuspendingdeferral-complete.md) | Notifica al sistema que la aplicación ha guardado sus datos y está lista para suspenderse.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
