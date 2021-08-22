---
title: Método SystemMonitor.Relog
description: Vuelve a cargar los datos del contador en un nuevo archivo. También puede usar este método para especificar un nuevo tipo de archivo y reducir el número de muestras contenidas en el archivo de registro.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Método SysMon de relog
- Método Relog SysMon , Objeto SystemMonitor
- Objeto SystemMonitor SysMon, método Relog
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
ms.openlocfilehash: 73025a352ba3ec2e9ed113c59a7e04f98084495da834f83bf052c697833dd13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881732"
---
# <a name="systemmonitorrelog-method"></a>Método SystemMonitor.Relog

Vuelve a cargar los datos del contador en un nuevo archivo. También puede usar este método para especificar un nuevo tipo de archivo y reducir el número de muestras contenidas en el archivo de registro.

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

*fileName* \[ En\]
</dt> <dd>

Ruta de acceso del archivo de registro. Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser .blg, .tsv o .csv. Si no existe una carpeta en la ruta de acceso, SYSMON la creará. Si el archivo existe, el archivo se sobrescribe. SYSMON aplica las ACL predeterminadas desde el directorio primario.

</dd> <dt>

*fileType* \[ En\]
</dt> <dd>

Formato de los datos del contador guardados en el archivo de registro. Puede especificarSysmonFileType.sys [**monFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv** o **SysmonFileType.sysmonFileTsv**.

</dd> <dt>

*filter* \[ En\]
</dt> <dd>

Número de ejemplos de los archivos de registro antiguos que se guardarán en el nuevo archivo de registro. Especifique 1 para guardar cada ejemplo de los archivos antiguos en los nuevos archivos. Especifique 2 para guardar uno de cada dos ejemplos del archivo antiguo. Especifique 3 para guardar uno de cada tres ejemplos del archivo antiguo. y así sucesivamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método usa los archivos de registro contenidos en la [**colección SystemMonitor.LogFiles**](systemmonitor-logfiles.md) para volver a registrar los datos del contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





