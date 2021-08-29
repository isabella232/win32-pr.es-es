---
description: Solicita que el dispositivo vuelva a establecer su configuración, configuración o información de estado desde un almacén de respaldo.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Método RestoreProperties de la CIM_LogicalDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2472ca36acbc152340dc0b47a2a353d6ad168f88af560f1753994df70a81dde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046855"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Método RestoreProperties de la clase \_ LogicalDevice de CIM

Solicita que el dispositivo vuelva a establecer su configuración, configuración o información de estado desde un almacén de respaldo. La intención es capturar esta información en un momento anterior (a través del método SaveProperties) y usarla para devolver un dispositivo a esta "condición" anterior. Es posible que este método no sea compatible con todos los dispositivos. El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y algún otro valor si se produjo algún otro error. En una subclase, se podría especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método . Las cadenas a las que se "traduce" el contenido de ValueMap también se pueden especificar en la subclase como calificador de matriz Values.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




