---
description: Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'IVmApplicationHealthMonitor:: SetApplicationState (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687195"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>IVmApplicationHealthMonitor:: SetApplicationState (método)

Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Representación **BSTR** del **GUID** que identifica la aplicación. Es responsabilidad de la aplicación que llama a crear y mantener los identificadores que usa para las aplicaciones que se están supervisando.

</dd> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Nombre para mostrar de la aplicación. Este nombre se usa en una entrada del registro de eventos informativos para el cambio de estado.

</dd> <dt>

*Estado* \[ de de\]
</dt> <dd>

Un valor de la enumeración del [**\_ Estado**](application-state.md) de la aplicación que especifica el nuevo estado de mantenimiento de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El estado de las aplicaciones que se ejecutan en la máquina virtual se refleja en el \[ valor de la propiedad OperationalStatus 1 \] de la clase [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .

Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                      |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




