---
title: Propiedad SystemMonitor. LogFileName
description: Recupera o establece el nombre de un archivo de registro que se va a utilizar como origen de los valores de contador mostrados en el monitor de sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propiedad nombreDeArchivoDeRegistro SysMon
- Propiedad nombreDeArchivoDeRegistro SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad nombreDeArchivoDeRegistro
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422336"
---
# <a name="systemmonitorlogfilename-property"></a>Propiedad SystemMonitor. LogFileName

Recupera o establece el nombre de un archivo de registro que se va a utilizar como origen de los valores de contador mostrados en el monitor de sistema.

> [!Note]  
> Esta propiedad ha quedado obsoleta en la propiedad [**logfiles**](systemmonitor-logfiles.md) .

 

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso al archivo de registro. Puede especificar una ruta de acceso absoluta, relativa o UNC. La extensión de nombre de archivo de registro debe ser. csv,. TSV o. BLG.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción                                  | Condición                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | No se puede encontrar el archivo especificado. El valor de Err. number es 0xC0000BD1. |
| **System.ArgumentException**                    | No se puede especificar una cadena vacía.                                    |



 

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve el nombre del archivo de registro del primer miembro de la colección [**logfiles**](systemmonitor-logfiles.md) .

Si se establece esta propiedad, se producirá un error si la colección [**logfiles**](systemmonitor-logfiles.md) contiene uno o más miembros.

Debe usar la herramienta Logman.exe o el complemento MMC Perfmon. msc para generar los archivos de registro que se agregan a esta colección. En el caso de Perfmon. msc, los registros de contador se encuentran en **registros y alertas de rendimiento**. Para obtener información detallada sobre el uso de Logman.exe o Perfmon. msc, busque Logman o use performance, respectivamente, en el **centro de ayuda y soporte técnico**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





