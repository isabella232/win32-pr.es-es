---
title: Método SetServerWeight de la clase Win32_TSSessionDirectory
description: Establece el valor de peso del servidor para el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Método SetServerWeight Servicios de Escritorio remoto
- Método SetServerWeight Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetServerWeight
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
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491608"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a>Método SetServerWeight de la \_ clase TSSessionDirectory de Win32

Establece el valor de peso del servidor para el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerWeightValue* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Valor del peso del servidor. El intervalo válido es de 1 a 10000.

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, en la interfaz de usuario de Servicios de Escritorio remoto configuración, el valor de peso del servidor es 100. El peso del servidor es relativo. Por lo tanto, si asigna un valor de a un servidor de 100 y un valor de 200, el servidor con un peso relativo de 200 recibirá dos veces el número de sesiones.

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

 

