---
title: SystemMonitor. relog (método)
description: Vuelve a registrar los datos del contador en un nuevo archivo. También puede utilizar este método para especificar un nuevo tipo de archivo y para reducir el número de ejemplos que contiene el archivo de registro.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog (método) SysMon
- Método relog SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150162"
---
# <a name="systemmonitorrelog-method"></a>SystemMonitor. relog (método)

Vuelve a registrar los datos del contador en un nuevo archivo. También puede utilizar este método para especificar un nuevo tipo de archivo y para reducir el número de ejemplos que contiene el archivo de registro.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre de archivo* \[ de\]
</dt> <dd>

Ruta de acceso del archivo de registro. Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser. BLG,. TSV o. csv. Si no existe una carpeta en la ruta de acceso, SYSMON la creará. Si el archivo existe, se sobrescribe el archivo. SYSMON aplica las ACL predeterminadas del directorio principal.

</dd> <dt>

*filetype* \[ de\]
</dt> <dd>

Formato de los datos de contador guardados en el archivo de registro. Puede especificar [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** o **SysmonFileType.sysmonFileTsv**.

</dd> <dt>

*filtro* \[ de de\]
</dt> <dd>

Número de muestras de los archivos de registro antiguos que se van a guardar en el nuevo archivo de registro. Especifique 1 para guardar todos los ejemplos de los archivos antiguos en los nuevos archivos. Especifique 2 para guardar una de cada dos muestras del archivo anterior. Especifique 3 para guardar una de cada tres muestras del archivo anterior. y así sucesivamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método usa los archivos de registro contenidos en la colección [**SystemMonitor. logfiles**](systemmonitor-logfiles.md) para reregistrar los datos del contador.

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

[**SystemMonitor. SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





