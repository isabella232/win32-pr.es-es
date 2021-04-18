---
title: SystemMonitor. SaveAs (método)
description: Guarda los valores del contador en la vista del gráfico en un archivo de registro.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Método SaveAs SysMon
- Método SaveAs SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665981"
---
# <a name="systemmonitorsaveas-method"></a>SystemMonitor. SaveAs (método)

Guarda los valores del contador en la vista del gráfico en un archivo de registro.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre de archivo* \[ de\]
</dt> <dd>

Ruta de acceso del archivo de registro. Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser. TSV o. htm. Si no existe una carpeta en la ruta de acceso, SYSMON la creará. Si el archivo existe, se sobrescribe el archivo. SYSMON aplica las ACL predeterminadas del directorio principal.

</dd> <dt>

*filetype* \[ de\]
</dt> <dd>

Formato de los datos de contador guardados en el archivo de registro. Puede especificar [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) o **SysmonFileType.sysmonFileTsv**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se guardan los datos del contador visibles en la vista del gráfico (para el número real de puntos de datos guardados, vea [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





