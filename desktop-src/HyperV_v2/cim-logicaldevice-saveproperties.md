---
description: Solicita que el dispositivo Capture su configuración actual, la configuración o la información de estado en una memoria auxiliar.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688455"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Método SaveProperties de la clase de LogicalDevice de CIM \_

Solicita que el dispositivo Capture su configuración actual, la configuración o la información de estado en una memoria auxiliar. El objetivo sería usar esta información más adelante (a través del método RestoreProperties) para devolver un dispositivo a su "condición" actual. Es posible que este método no sea compatible con todos los dispositivos. El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y otro valor si se produjo algún otro error. En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método. También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




