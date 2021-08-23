---
description: Restablezca la configuración activa del recopilador desde el archivo de copia de seguridad posterior (determinado a partir de la marca de tiempo original actual). Si la configuración se ha deshace, significa volver a hacer el cambio deshacer.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Método Redo de la clase Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 45f8d2c8ae34ae3f045a579cbb588f1a67e635077951c10916655788b48f7795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579515"
---
# <a name="redo-method-of-the-control-class"></a>Método Redo de la clase Control

Restablezca la configuración activa del recopilador desde el archivo de copia de seguridad posterior (determinado a partir de la marca de tiempo original actual). Si la configuración se ha deshace, significa volver a hacer el cambio deshacer.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 Redo(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
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

Marca de tiempo de cuando se estableció la configuración anterior. Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se cambió entre sí). Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OldTimestampHigh* \[ En\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración anterior. Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se cambió entre sí). Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Marca de tiempo de cuándo se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Marca de tiempo de cuándo se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Marca de tiempo original de cuando se estableció la configuración restaurada por primera vez. Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Marca de tiempo original de cuando se estableció la configuración restaurada por primera vez. Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

