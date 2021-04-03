---
description: El método SetPowerState establece el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.
ms.assetid: 9a8be1bb-f5ca-4b82-bea1-30090c7e2569
ms.tgt_platform: multiple
title: Método SetPowerState de la clase CIM_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 107a4a8df69cb5e5e9e4cf781f52d88ff37e3fba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907330"
---
# <a name="setpowerstate-method-of-the-cim_desktopmonitor-class"></a>Método SetPowerState de la \_ clase CIM DesktopMonitor

El método **SetPowerState** establece el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado. En una subclase, el conjunto de códigos de retorno posibles se debe especificar mediante un calificador **ValueMap** en el método. Las cadenas a las que se traduce el contenido **ValueMap** también se deben especificar en la subclase como calificador de matriz **Values** . Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PowerState* \[ de\]
</dt> <dd>

Un valor **ValueMap** que especifica el estado de energía deseado para este dispositivo lógico.

<dt>

1
</dt> <dd>

Potencia completa.

</dd> <dt>

2
</dt> <dd>

Ahorro de energía: modo de baja energía.

</dd> <dt>

3
</dt> <dd>

Ahorro de energía en espera.

</dd> <dt>

4
</dt> <dd>

Ahorro de energía: otros.

</dd> <dt>

5
</dt> <dd>

Ciclo de energía.

</dd> <dt>

6
</dt> <dd>

Desconectar.

</dd> </dl> </dd> <dt>

*Hora* \[ de de\]
</dt> <dd>

Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método). Cuando el parámetro *PowerState* es igual a 5 ("ciclo de energía"), el parámetro *Time* indica cuándo debe volver a encenderse el dispositivo. El apagado es inmediato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si es correcto, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificada y otro valor si se produjo algún otro error.

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[\_DESKTOPMONITOR CIM](setpowerstate-method-in-class-cim-desktopmonitor.md)
</dt> <dt>

[**\_DESKTOPMONITOR CIM**](cim-desktopmonitor.md)
</dt> </dl>

 

 




