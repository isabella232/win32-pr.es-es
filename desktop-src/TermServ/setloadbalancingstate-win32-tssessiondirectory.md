---
title: Método SetLoadBalancingState de la Win32_TSSessionDirectory clase
description: Establece el valor para indicar si el servidor participará en el equilibrio de carga Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Método SetLoadBalancingState Servicios de Escritorio remoto
- Método SetLoadBalancingState Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259004"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Método SetLoadBalancingState de la clase TSSessionDirectory de Win32 \_

Establece el valor para indicar si el servidor participará en el equilibrio de carga Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StateValue* \[ En\]
</dt> <dd>

Tipo: **uint32**

Indica si el servidor participará en el equilibrio de carga del Agente de conexión a Escritorio remoto.

<dt>

0
</dt> <dd>

El servidor no participará en el equilibrio de carga del Agente de conexión a Escritorio remoto.

</dd> <dt>

1
</dt> <dd>

El servidor participará en el equilibrio de carga del Agente de conexión a Escritorio remoto.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor debe estar unido a una granja en el Agente de conexión a Escritorio remoto.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

