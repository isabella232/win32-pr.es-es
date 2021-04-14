---
description: Proporciona información sobre una operación de suspensión de la aplicación.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaz ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541654"
---
# <a name="isuspendingoperation-interface"></a>Interfaz ISuspendingOperation

Proporciona información sobre una operación de suspensión de la aplicación.

## <a name="members"></a>Miembros

La interfaz **ISuspendingOperation** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ISuspendingOperation** tiene estos métodos.



| Método                                                  | Descripción                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Solicita que se retrase la operación de suspensión de la aplicación.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **ISuspendingOperation** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Fecha límite**](isuspendingoperation-deadline.md)<br/> | Lectura/escritura<br/> | Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicación retrasada.<br/> |



 

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

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
