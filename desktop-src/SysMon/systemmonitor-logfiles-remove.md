---
title: Método LogFiles.Remove
description: Quita la instancia de LogFileItem especificada de la colección.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Método Remove SysMon
- Método Remove SysMon , clase LogFiles
- Clase LogFiles SysMon , método Remove
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
ms.openlocfilehash: c12c0bae91df3baf421638665a5587612e6d1404c3300cf02b0308b7bef7d016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955445"
---
# <a name="logfilesremove-method"></a>Método LogFiles.Remove

Quita la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.

## <a name="syntax"></a>Sintaxis


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice entero del archivo de registro que se quitará de la colección. El índice se basa en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

**Antes de Windows Vista:** No se pueden quitar [](systemmonitor-logfiles.md) archivos de registro de la colección de archivos de registro si el valor de [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) está establecido en sysmonLogFiles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





