---
title: Propiedad SystemMonitor.LogFileName
description: Recupera o establece el nombre de un archivo de registro que se usará como origen de los valores de contador mostrados en el Monitor de sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propiedad LogFileName SysMon
- Propiedad LogFileName SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad LogFileName
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
ms.openlocfilehash: 888ecf566dd30b12cde8e9105c987cf5f76afd3578ef9b8f4aee3b8d38e5710f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955543"
---
# <a name="systemmonitorlogfilename-property"></a>Propiedad SystemMonitor.LogFileName

Recupera o establece el nombre de un archivo de registro que se usará como origen de los valores de contador mostrados en el Monitor de sistema.

> [!Note]  
> Esta propiedad se ha quedado obsoleta por la [**propiedad LogFiles.**](systemmonitor-logfiles.md)

 

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso al archivo de registro. Puede especificar una ruta de acceso UNC, relativa o absoluta. La extensión de nombre de archivo de registro debe ser .csv, .tsv o .blg.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción                                  | Condición                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System.Runtime.InteropServices.COMException** | No se encuentra el archivo especificado. El valor Err.Number es 0xC0000BD1. |
| **System.ArgumentException**                    | No se puede especificar una cadena vacía.                                    |



 

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve el nombre del archivo de registro del primer miembro de la [**colección LogFiles.**](systemmonitor-logfiles.md)

Se producirá un error al establecer esta propiedad si la [**colección LogFiles**](systemmonitor-logfiles.md) contiene uno o varios miembros.

Debe usar la herramienta Logman.exe o el complemento MMC Perfmon.msc para generar los archivos de registro que agregue a esta colección. Para Perfmon.msc, los registros de contador se encuentran en **Registros y alertas de rendimiento**. Para obtener más información sobre Logman.exe o Perfmon.msc, busque Logman o Using Performance, respectivamente, en el **Centro de ayuda y soporte técnico**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





