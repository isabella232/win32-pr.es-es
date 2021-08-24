---
description: Si la configuración actual es el resultado de deshacer, rehacer o restaurar, marca como si se hubiera establecido explícitamente, de modo que el historial conserve la hora en que se estableció y se creará un archivo de copia de seguridad para él en el siguiente cambio de configuración.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Método Checkpoint de la clase Control (Srrestoreptapi.h)
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
ms.openlocfilehash: ff71086703e409331e420fd064f73ff2406ec4e5167ea97da78b2afc498bf244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579855"
---
# <a name="checkpoint-method-of-the-control-class"></a>Método Checkpoint de la clase Control

Si la configuración actual es el resultado de deshacer, rehacer o restaurar, marca como si se hubiera establecido explícitamente, de modo que el historial conserve la hora en que se estableció y se creará un archivo de copia de seguridad para él en el siguiente cambio de configuración. Si la configuración actual ya se estableció explícitamente, no tiene ningún efecto.

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

*OldTimestampLow* \[ En\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual. Si no es 0, habilita la comprobación de atomicidad: la acción solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se cambió entre sí). Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OldTimestampHigh* \[ En\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración actual. Si no es 0, habilita la comprobación de atomicidad: la acción solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se cambió entre sí). Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Cadena de texto con una explicación del error.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Cadena de texto con advertencias.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Cadena de texto con información sobre la configuración.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Tipo del error. Tenga en cuenta que 0 o absent indica que se ha hecho correctamente.

<dt>

0
</dt> <dd>

Correcto.

</dd> <dt>

1
</dt> <dd>

formato de argumento no válido

</dd> <dt>

2
</dt> <dd>

valor de argumento no válido

</dd> <dt>

3
</dt> <dd>

error de apertura del recurso (socket)

</dd> <dt>

4
</dt> <dd>

error de persistencia (escritura de archivos)

</dd> <dt>

5
</dt> <dd>

error de atomicidad (la marca de tiempo anterior no coincide)

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz \\ de Microsoft Windows \\ \\ BootEventCollector<br/>                                              |
| Header<br/>                   | <dl> <dt>Srrestoreptapi.h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

