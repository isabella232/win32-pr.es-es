---
description: Restablezca la configuración activa del recopilador del archivo de copia de seguridad posterior (determinado por el avance desde la marca de tiempo original actual). Si se ha deshecho la configuración, significa que se rehace el cambio deshecho.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Método redo de la clase control
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
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152774"
---
# <a name="redo-method-of-the-control-class"></a>Método redo de la clase control

Restablezca la configuración activa del recopilador del archivo de copia de seguridad posterior (determinado por el avance desde la marca de tiempo original actual). Si se ha deshecho la configuración, significa que se rehace el cambio deshecho.

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

