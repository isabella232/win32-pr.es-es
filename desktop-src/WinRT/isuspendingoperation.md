---
description: Proporciona información sobre una operación de suspensión de aplicaciones.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaz ISuspendingOperation (Windows. ApplicationModel.h)
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
ms.openlocfilehash: f17cd3d3b1eab67d0abfea200e657d8c4a17d8df9e3bb850e4ea361a760d19df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758635"
---
# <a name="isuspendingoperation-interface"></a>Interfaz ISuspendingOperation

Proporciona información sobre una operación de suspensión de aplicaciones.

## <a name="members"></a>Miembros

La **interfaz ISuspendingOperation** hereda de [**IInspectable.**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) **ISuspendingOperation** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ISuspendingOperation** tiene estos métodos.



| Método                                                  | Descripción                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Solicita que la operación de suspensión de la aplicación se retrase.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz ISuspendingOperation** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Fecha límite**](isuspendingoperation-deadline.md)<br/> | Lectura/escritura<br/> | Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicaciones retrasada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
