---
description: El método ResetCounter restablece los contadores de error y advertencia.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Método ResetCounter de la CIM_DeviceErrorCounts clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892556"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>Método ResetCounter de la clase \_ DeviceErrorCounts de CIM

El **método ResetCounter** restablece los contadores de error y advertencia. Se usa un método para que la instrumentación del dispositivo lógico, que tabula los errores y advertencias, también pueda restablecer el procesamiento interno y los contadores. En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido **de ValueMap** también se pueden especificar en la subclase como calificador de **matriz Values.**

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SelectedCounter* \[ En\]
</dt> <dd>

Contador de errores que se debe restablecer.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Todos** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Contador de errores indeterminado** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Contador de errores críticos** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Contador de errores principales** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Contador de errores menores** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Contador de** advertencia (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite y cualquier otro valor si se produjo un error.

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ DeviceErrorCounts](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> </dl>

 

