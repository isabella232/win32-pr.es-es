---
description: Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de error incrustadas MSVM \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Método FormatError de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666562"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método FormatError de la \_ clase VirtualSystemManagementService de MSVM

Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de [**\_ error**](msvm-error.md) incrustadas MSVM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ de de\]
</dt> <dd>

Tipo: **String \[ \]**

Matriz de cadenas que contiene las instancias de [**\_ error de MSVM**](msvm-error.md) utilizadas para generar el mensaje de error de salida.

</dd> <dt>

*ErrorMessage* \[ enuncia\]
</dt> <dd>

Tipo: **String**

En la salida, cadena que contiene los mensajes de error concatenados representados por las instancias de [**\_ error MSVM**](msvm-error.md) que se han pasado en *el parámetro* Errors. Cada cadena de error está separada por un par de caracteres de nueva línea (' \\ n ').

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

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

El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

