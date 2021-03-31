---
title: Propiedad DataSourceType SystemMonitor
description: Recupera o establece el origen de los datos del contador de rendimiento.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propiedad DataSourceType SysMon
- Propiedad DataSourceType SysMon, interfaz SystemMonitor
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
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079587"
---
# <a name="systemmonitordatasourcetype-property"></a>SystemMonitor::D propiedad ataSourceType

Recupera o establece el origen de los datos del contador de rendimiento.

## <a name="syntax"></a>Sintaxis


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Valor de propiedad

Origen de los datos del contador de rendimiento. Para obtener los valores posibles, vea [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Excepciones



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de excepción</th>
<th>Condición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System.ArgumentException</strong></td>
<td>Puede recibir esta excepción por una de las siguientes razones:
<ul>
<li>El valor de origen de datos especificado no es válido.</li>
<li>Si el origen de datos es un archivo de registro, SYSMON no puede encontrar uno de los archivos especificados. El valor de Err. number es 0xC0000BD1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

**Antes de Windows Vista:** No puede Agregar o quitar archivos de registro de la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de esta propiedad se establece en sysmonLogFiles. Establezca el valor de esta propiedad en sysmonLogFiles después de crear o modificar la colección de archivos de registro.

Además, no se pueden modificar las propiedades [**SqlDsnName**](systemmonitor-sqldsnname.md) y [**SqlLogSetName**](systemmonitor-sqllogsetname.md) si el valor de esta propiedad no se debe establecer en sysmonSqlLog. Establezca el valor de esta propiedad en sysmonSqlLog después de modificar los nombres del servidor y de la base de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





