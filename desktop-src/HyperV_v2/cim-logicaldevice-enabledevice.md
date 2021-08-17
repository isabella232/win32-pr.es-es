---
description: El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Método EnableDevice de la CIM_LogicalDevice clase
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
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648530"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>Método EnableDevice de la clase \_ LogicalDevice de CIM

El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.

Solicita que el dispositivo lógico esté habilitado ("Habilitado" parámetro de entrada = TRUE) o deshabilitado (= FALSE). Si se realiza correctamente, las propiedades StatusInfo/EnabledState del dispositivo deben reflejar el estado deseado (habilitado o deshabilitado). Tenga en cuenta que la función de este método se superpone con la propiedad RequestedState. RequestedState se agregó al modelo para mantener un registro (es decir, un valor persistente) de la última solicitud de estado. La invocación del método EnableDevice debe establecer la propiedad RequestedState correctamente.

El código de retorno debe ser 0 si la solicitud se ejecutó correctamente, 1 si no se admite la solicitud y algún otro valor si se produjo un error. En una subclase, se podría especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método . Las cadenas a las que se "traduce" el contenido de ValueMap también se pueden especificar en la subclase como calificador de matriz Values.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ En\]
</dt> <dd>

Si es TRUE, habilite el dispositivo, si es FALSE, deshabilite el dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




