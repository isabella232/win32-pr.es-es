---
description: Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: IVmApplicationHealthMonitor::SetApplicationState (método)
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
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392360"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>IVmApplicationHealthMonitor::SetApplicationState (método)

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

*Id.* \[ en\]
</dt> <dd>

Representación **BSTR** del **GUID** que identifica la aplicación. Es responsabilidad de la aplicación que realiza la llamada crear y mantener los identificadores que usa para las aplicaciones que se supervisan.

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre para mostrar de la aplicación. Este nombre se usa en una entrada del registro de eventos informativos para el cambio de estado.

</dd> <dt>

*Estado* \[ En\]
</dt> <dd>

Valor de la [**enumeración APPLICATION \_ STATE**](application-state.md) que especifica el nuevo estado de mantenimiento de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El estado de las aplicaciones que se ejecutan en la máquina virtual se refleja en el valor de la propiedad **OperationalStatus** 1 de \[ la clase \] [**\_ HeartbeatComponent de Msvm.**](msvm-heartbeatcomponent.md)

Para usar este elemento de programación, Windows 8 componentes de integración deben instalarse en la máquina virtual en la que se ejecuta la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                      |
| Versión<br/>                  | Componentes de integración para Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




