---
description: Solicita que el dispositivo capture su configuración, configuración o información de estado actuales en un almacén de respaldo.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties de la CIM_LogicalDevice clase
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
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648167"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>Método SaveProperties de la clase \_ LogicalDevice de CIM

Solicita que el dispositivo capture su configuración, configuración o información de estado actuales en un almacén de respaldo. El objetivo sería usar esta información más adelante (a través del método RestoreProperties) para devolver un dispositivo a su "condición" actual. Es posible que este método no sea compatible con todos los dispositivos. El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y algún otro valor si se produjo algún otro error. En una subclase, se podría especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método . Las cadenas a las que se "traduce" el contenido de ValueMap también se pueden especificar en la subclase como calificador de matriz Values.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




