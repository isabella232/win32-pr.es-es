---
description: Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de error de Msvm \_ insertadas.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Método FormatError de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b7f2ba03c21c08af3b9249c0ee3099291fdd190d22516ed503c012dae63f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253955"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método FormatError de la clase Msvm \_ VirtualSystemManagementService

Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de [**\_ error de Msvm**](msvm-error.md) insertadas.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ En\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz de cadenas que contienen instancias [**de \_ error de Msvm**](msvm-error.md) usadas para generar el mensaje de error de salida.

</dd> <dt>

*ErrorMessage* \[ out\]
</dt> <dd>

Tipo: **cadena**

En la salida, una cadena que contiene los mensajes de error concatenados representados por las instancias de error de [**Msvm \_**](msvm-error.md) pasadas en el *parámetro Errors.* Cada cadena de error está separada por un par de caracteres de nueva línea \\ ('n').

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a [**la clase Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

