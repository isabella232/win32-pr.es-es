---
description: El método SetPowerState de la clase MediaAccessDevice de CIM establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo \_ en ese estado.
ms.assetid: 298938c5-fa66-456c-892c-9dd348aa9739
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_MediaAccessDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b32faecd35466a08d2fa18a927c0c292be7ef8f3c76659824e015d1adbb3b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119578295"
---
# <a name="setpowerstate-method-of-the-cim_mediaaccessdevice-class"></a>Método SetPowerState de la clase \_ MediaAccessDevice de CIM

El **método SetPowerState** de la clase MediaAccessDevice de CIM establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo \_ en ese estado. En una subclase, el conjunto de códigos de retorno posibles debe especificarse mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido de **ValueMap** también se deben especificar en la subclase como calificador de **matriz Values.** Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Potencia completa.

</dd> <dt>

2
</dt> <dd>

Ahorro de energía en modo de bajo consumo.

</dd> <dt>

3
</dt> <dd>

Ahorro de energía en espera.

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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CIM \_ MediaAccessDevice](setpowerstate-method-in-class-cim-mediaaccessdevice.md)
</dt> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




