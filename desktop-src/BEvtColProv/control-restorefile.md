---
description: Restaure la configuración activa del recopilador desde un archivo de copia de seguridad.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Método RestoreFile de la clase Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 148b35199822c98ca03041561f402dc5acaadddf067b9eeecd80e9b32e325db2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589115"
---
# <a name="restorefile-method-of-the-control-class"></a>Método RestoreFile de la clase Control

Restaure la configuración activa del recopilador desde un archivo de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 RestoreFile(
  [in]  string File,
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

*Archivo* \[ En\]
</dt> <dd>

Nombre del archivo de copia de seguridad que se restaurará, de la lista devuelta por ListBackups().

</dd> <dt>

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

Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte baja de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte alta de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

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

Tipo del error: tenga en cuenta que 0 o absent indica que se ha producido correctamente.

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



| Requisito | Value |
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

 

