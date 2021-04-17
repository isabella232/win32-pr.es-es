---
description: El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Método EnableDevice de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667841"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Método EnableDevice de la clase de LogicalDevice de CIM \_

El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.

Solicita que el LogicalDevice esté habilitado ("habilitado" parámetro de entrada = TRUE) o deshabilitado (= FALSE). Si es correcto, las propiedades de StatusInfo/EnabledState del dispositivo deben reflejar el estado deseado (habilitado o deshabilitado). Tenga en cuenta que la función de este método se superpone con la propiedad RequestedState. RequestedState se ha agregado al modelo para mantener un registro (es decir, un valor almacenado) de la última solicitud de estado. Al invocar el método EnableDevice se debe establecer la propiedad RequestedState adecuadamente.

El código de retorno debe ser 0 si la solicitud se ejecutó correctamente, 1 si no se admite la solicitud y otro valor si se produjo un error. En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método. También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Si es TRUE, habilite el dispositivo, si es FALSE, deshabilite el dispositivo.

</dd> </dl>

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

 

 




