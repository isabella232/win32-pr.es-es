---
title: Propiedad SystemMonitor DataSourceType
description: Recupera o establece el origen de los datos del contador de rendimiento.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propiedad SysMon de DataSourceType
- Propiedad SysMon de DataSourceType, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79adffc396a581daee16218fc5d39a6480805f0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481861"
---
# <a name="systemmonitordatasourcetype-property"></a>Propiedad SystemMonitor::D ataSourceType

Recupera o establece el origen de los datos del contador de rendimiento.

## <a name="syntax"></a>Syntax


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Valor de propiedad

Origen de los datos del contador de rendimiento. Para ver los valores posibles, [**vea DataSourceTypeConstants.**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants)

## <a name="exceptions"></a>Excepciones




| Tipo de excepción | Condición | 
|----------------|-----------|
| <strong>System.ArgumentException</strong> | Puede recibir esta excepción por uno de los siguientes motivos:<ul><li>El valor de origen de datos especificado no es válido.</li><li>Si el origen de datos es un archivo de registro, SYSMON no puede encontrar uno de los archivos especificados. El valor Err.Number es 0xC0000BD1.</li></ul> | 




 

## <a name="remarks"></a>Comentarios

**Antes de Windows Vista:** No puede agregar ni quitar [](systemmonitor-logfiles.md) archivos de registro de la colección de archivos de registro si el valor de esta propiedad está establecido en sysmonLogFiles. Establezca solo el valor de esta propiedad en sysmonLogFiles después de crear o modificar la colección de archivos de registro.

Además, no puede modificar las [**propiedades SqlDsnName**](systemmonitor-sqldsnname.md) y [**SqlLogSetName**](systemmonitor-sqllogsetname.md) si el valor de esta propiedad no debe establecerse en sysmonSqlLog. Establezca solo el valor de esta propiedad en sysmonSqlLog después de modificar los nombres de servidor y base de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





