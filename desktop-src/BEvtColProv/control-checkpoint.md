---
description: Si la configuración actual es el resultado de la operación de deshacer/rehacer/restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad en el siguiente cambio de configuración.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Método Checkpoint de la clase control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152777"
---
# <a name="checkpoint-method-of-the-control-class"></a>Método Checkpoint de la clase control

Si la configuración actual es el resultado de la operación de deshacer/rehacer/restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad en el siguiente cambio de configuración. Si la configuración actual ya estaba establecida explícitamente, no tiene ningún efecto.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldTimestampLow* \[ de\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual. Si no es 0, habilita la comprobación de atomicidad: la acción se aplicará únicamente si la marca de tiempo de la configuración anterior coincide (es decir, si la configuración no se ha cambiado entre). Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ de\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual. Si no es 0, habilita la comprobación de atomicidad: la acción se aplicará únicamente si la marca de tiempo de la configuración anterior coincide (es decir, si la configuración no se ha cambiado entre). Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ enuncia\]
</dt> <dd>

Cadena de texto con la explicación del error.

</dd> <dt>

*WarningString* \[ enuncia\]
</dt> <dd>

Cadena de texto con advertencias.

</dd> <dt>

*InfoString* \[ enuncia\]
</dt> <dd>

Cadena de texto con información sobre la configuración.

</dd> <dt>

*ErrorType* \[ enuncia\]
</dt> <dd>

Tipo del error. Tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.

<dt>

0
</dt> <dd>

Correcto.

</dd> <dt>

1
</dt> <dd>

formato de argumento incorrecto

</dd> <dt>

2
</dt> <dd>

valor de argumento no válido

</dd> <dt>

3
</dt> <dd>

error de recurso abierto de recursos (socket)

</dd> <dt>

4
</dt> <dd>

error de persistencia (escritura de archivo)

</dd> <dt>

5
</dt> <dd>

error de atomicidad (la marca de tiempo anterior no coincidía)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

<dl> <dt>


</dt> <dd>

0

Error

</dd> <dt>


</dt> <dd>

1

Correcto

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>Srrestoreptapi. h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

