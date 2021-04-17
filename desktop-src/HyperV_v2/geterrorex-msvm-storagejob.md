---
description: Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna \_ instancia de error MSVM.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Método GetErrorEx de la clase Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666553"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a>Método GetErrorEx de la \_ clase StorageJob de MSVM

Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) . Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ de enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Si el estado operativo del trabajo no es "correcto", este método devuelve una matriz de instancias [**de \_ error de MSVM**](msvm-error.md) . De lo contrario, si el trabajo es "OK", se devuelve **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase [**MSVM \_ StorageJob**](msvm-storagejob.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ StorageJob**](msvm-storagejob.md)
</dt> </dl>

 

