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
ms.openlocfilehash: 23d539f07c97e4e5b92152190a7bb38a8132d31a73daf08de8f140a39f67efdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987955"
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

## <a name="remarks"></a>Comentarios

El servidor debe estar unido a una granja en el Agente de conexión a Escritorio remoto.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

