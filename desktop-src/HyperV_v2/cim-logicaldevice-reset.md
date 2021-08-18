---
description: Solicita un restablecimiento de LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Método de restablecimiento de la CIM_LogicalDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81f69f57af9d8633874a6b3713ff85cd1342c9df56b22924096619b834f1b867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648540"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Método de restablecimiento de la CIM_LogicalDevice (administración de Hyper-V)

Solicita un restablecimiento de LogicalDevice. En una subclase, se podría especificar el conjunto de códigos de retorno posibles, mediante un calificador ValueMap en el método . Las cadenas a las que se "traduce" el contenido de ValueMap también se pueden especificar en la subclase como calificador de matriz Values.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




