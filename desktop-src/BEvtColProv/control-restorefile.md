---
description: Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Método RestoreFile de la clase control
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
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998083"
---
# <a name="restorefile-method-of-the-control-class"></a>Método RestoreFile de la clase control

Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad.

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

*Archivo* \[ de de\]
</dt> <dd>

Nombre del archivo de copia de seguridad que se va a restaurar, en la lista devuelta por ListBackups ().

</dd> <dt>

*OldTimestampLow* \[ de\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración anterior. Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre). Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ de\]
</dt> <dd>

Marca de tiempo de cuando se estableció la configuración anterior. Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre). Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ enuncia\]
</dt> <dd>

Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ enuncia\]
</dt> <dd>

Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente. Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ enuncia\]
</dt> <dd>

Marca de tiempo original de la primera vez que se estableció la configuración restaurada. Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ enuncia\]
</dt> <dd>

Marca de tiempo original de la primera vez que se estableció la configuración restaurada. Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

El tipo del error: tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

