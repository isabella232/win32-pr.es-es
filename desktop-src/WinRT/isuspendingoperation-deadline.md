---
description: Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicaciones retrasada.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: Propiedad ISuspendingOperation::D eadline (Windows. ApplicationModel.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 448f4d89ec2f1b7e3f68255897b32b3f4cba2ec753ae8f6cc7751c9041b01266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121505"
---
# <a name="isuspendingoperationdeadline-property"></a>ISuspendingOperation::D eadline

Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicaciones retrasada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>Valor de propiedad

El tiempo restante antes de que continúe una operación de suspensión de aplicaciones retrasada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




