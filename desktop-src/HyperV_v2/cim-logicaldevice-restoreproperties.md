---
description: Solicita que el dispositivo vuelva a establecer la configuración, la configuración o la información de estado desde una memoria auxiliar.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Método RestoreProperties de la clase CIM_LogicalDevice
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
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668435"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Método RestoreProperties de la clase de LogicalDevice de CIM \_

Solicita que el dispositivo vuelva a establecer la configuración, la configuración o la información de estado desde una memoria auxiliar. La intención es capturar esta información en un momento anterior (a través del método SaveProperties) y usarla para devolver un dispositivo a esta "condición" anterior. Es posible que este método no sea compatible con todos los dispositivos. El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y otro valor si se produjo algún otro error. En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método. También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.

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
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

 




