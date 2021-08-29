---
description: El método SetPowerState de la clase Cim Printer establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo \_ en ese estado.
ms.assetid: 8a170dea-400a-4f2a-9402-f70a97d4a46c
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_Printer clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3d0fcc322f6ee855f72d64386998880a20b02b64e9a0d713f17f625cb64c5ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436755"
---
# <a name="setpowerstate-method-of-the-cim_printer-class"></a>Método SetPowerState de la clase \_ CIM Printer

El **método SetPowerState** de la clase Cim Printer establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo \_ en ese estado. En una subclase, el conjunto de códigos de retorno posibles debe especificarse mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido de **ValueMap** también se deben especificar en la subclase como calificador de **matriz Values.** Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PowerState* \[ En\]
</dt> <dd>

Valor **valueMap** que especifica el estado de energía deseado para este dispositivo lógico.

<dt>

1
</dt> <dd>

Energía completa.

</dd> <dt>

2
</dt> <dd>

Ahorro de energía en modo de bajo consumo.

</dd> <dt>

3
</dt> <dd>

Espera de ahorro de energía.

</dd> <dt>

4
</dt> <dd>

Otro ahorro de energía.

</dd> <dt>

5
</dt> <dd>

Ciclo de energía.

</dd> <dt>

6
</dt> <dd>

Apagar.

</dd> </dl> </dd> <dt>

*Hora* \[ En\]
</dt> <dd>

Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método). Cuando el *parámetro PowerState* es igual a 5 ("Ciclo de energía"), el parámetro *Time* indica cuándo se debe volver a encender el dispositivo. El apagado es inmediato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificadas y otro valor si se produjo cualquier otro error.

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresora \_ CIM](setpowerstate-method-in-class-cim-printer.md)
</dt> <dt>

[**Impresora \_ CIM**](cim-printer.md)
</dt> </dl>

 

 




