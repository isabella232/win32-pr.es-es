---
title: Método SetServerWeight de la Win32_TSSessionDirectory clase
description: Establece el valor de peso del servidor para el equilibrio de carga Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Método SetServerWeight Servicios de Escritorio remoto
- Método SetServerWeight Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto método , SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d8c9af7995f2d42f02075fde8ae43f4b5f5e9a5ccb7d3fa6f4635cb9645464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604634"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Método SetServerWeight de la clase TSSessionDirectory de Win32 \_

Establece el valor de peso del servidor para el equilibrio de carga Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerWeightValue* \[ En\]
</dt> <dd>

Tipo: **uint32**

Valor de peso del servidor. El intervalo válido es de 1 a 10 000.

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, en la interfaz de usuario de Servicios de Escritorio remoto Configuration, el valor de peso del servidor es 100. El peso del servidor es relativo. Por lo tanto, si asigna a un servidor un valor de 100 y otro un valor de 200, el servidor con un peso relativo de 200 recibirá el doble del número de sesiones.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

