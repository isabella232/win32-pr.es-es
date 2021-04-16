---
title: Método SetLoadBalancingState de la clase Win32_TSSessionDirectory
description: Establece el valor para indicar si el servidor participará en el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Método SetLoadBalancingState Servicios de Escritorio remoto
- Método SetLoadBalancingState Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetLoadBalancingState
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685920"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a>Método SetLoadBalancingState de la \_ clase TSSessionDirectory de Win32

Establece el valor para indicar si el servidor participará en el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StateValue* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Indica si el servidor participará en el equilibrio de carga del agente de conexión a escritorio remoto.

<dt>

0
</dt> <dd>

El servidor no participará en el equilibrio de carga del agente de conexión a escritorio remoto.

</dd> <dt>

1
</dt> <dd>

El servidor participará en el equilibrio de carga del agente de conexión a escritorio remoto.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El servidor debe estar unido a una granja de servidores en el agente de conexión a escritorio remoto.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

