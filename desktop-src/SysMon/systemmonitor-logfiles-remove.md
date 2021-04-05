---
title: LogFiles. Remove (método)
description: Quita la instancia de LogFileItem especificada de la colección.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Quitar método SysMon
- Remove (método) SysMon, logfiles (clase)
- Logfiles (clase) SysMon, Remove (método)
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803350"
---
# <a name="logfilesremove-method"></a>LogFiles. Remove (método)

Quita la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.

## <a name="syntax"></a>Sintaxis


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice de entero del archivo de registro que se va a quitar de la colección. El índice está basado en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**Antes de Windows Vista:** No se pueden quitar archivos de registro de la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en sysmonLogFiles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





