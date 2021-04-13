---
title: Counters. Add (método)
description: Agrega una instancia de un elemento de objeto a la colección.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Agregar método SysMon
- Agregar método SysMon, clase counters
- Counters (clase) SysMon, Add (método)
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489719"
---
# <a name="countersadd-method"></a>Counters. Add (método)

Agrega una instancia de un [**elemento de objeto**](counteritem.md) a la colección.

## <a name="syntax"></a>Sintaxis


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso al contador. La ruta de acceso puede incluir un nombre de equipo y debe incluir un nombre de objeto de rendimiento, un nombre de instancia de objeto si el objeto de rendimiento especificado admite varias instancias y un nombre de contador. Esta especificación de ruta de acceso no distingue entre mayúsculas y minúsculas.

Para obtener más información sobre cómo especificar una ruta de acceso de contador, consulte [especificar una ruta de acceso de contador](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

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
<td><strong>System. Runtime. InteropServices. COMException</strong></td>
<td>Puede recibir esta excepción por una de las siguientes razones:
<ul>
<li>No se encontró el objeto de rendimiento especificado en el equipo. El valor de Err. number es 0xC0000BB8.</li>
<li>No se pudo encontrar el contador especificado. El valor de Err. number es 0xC0000BB9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Si especifica un contador de caracteres comodín en el parámetro *PathName* , el método **Add** crea un objeto de [**peritem**](counteritem.md) para cada ruta de acceso expandida. A continuación, el método **Add** devuelve un puntero al primer **objeto** que se ha agregado.

Si el carácter comodín daría como resultado un contador duplicado, el error no se envía y no se crea ningún duplicado. Si se produce una condición de error antes de que se creen todos los contadores, se genera el error y no se crean los contadores restantes.

No hay ningún límite en el número de contadores que puede Agregar; sin embargo, SYSMON solo creará un gráfico de los primeros 1.024 contadores de la colección. No hay ningún límite en el número de contadores que SYSMON mostrará en un informe.

Para recibir una notificación cuando se agrega un contador, implemente el evento [OnCounterAdded](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

