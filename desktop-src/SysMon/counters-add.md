---
title: Método Counters.Add
description: Agrega una instancia counterItem a la colección.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Adición del método SysMon
- Agregar método SysMon , clase Counters
- Clase Counters SysMon , Add (método)
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
ms.openlocfilehash: a8d8169980de00338c7fdd0b804013f986a5a7ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068862"
---
# <a name="countersadd-method"></a>Método Counters.Add

Agrega una [**instancia counterItem**](counteritem.md) a la colección.

## <a name="syntax"></a>Sintaxis


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pathname* \[ En\]
</dt> <dd>

Ruta de acceso al contador. La ruta de acceso puede incluir un nombre de equipo y debe incluir un nombre de objeto de rendimiento, un nombre de instancia de objeto si el objeto de rendimiento especificado admite varias instancias y un nombre de contador. Esta especificación de ruta de acceso no distingue mayúsculas de minúsculas.

Para obtener más información sobre cómo especificar una ruta de acceso de contador, vea [Especificar una ruta de acceso de contador.](/windows/desktop/PerfCtrs/specifying-a-counter-path)

</dd> </dl>

## <a name="exceptions"></a>Excepciones




| Tipo de excepción | Condición | 
|----------------|-----------|
| <strong>System.Runtime.InteropServices.COMException</strong> | Puede recibir esta excepción por uno de los siguientes motivos:<ul><li>No se encontró el objeto de rendimiento especificado en el equipo. El valor Err.Number es 0xC0000BB8.</li><li>No se encontró el contador especificado. El valor Err.Number es 0xC0000BB9.</li></ul> | 




 

## <a name="remarks"></a>Observaciones

Si especifica un contador comodín en el parámetro *pathname,* el método **Add** crea un objeto [**CounterItem**](counteritem.md) para cada ruta de acceso expandida. A **continuación,** el método Add devuelve un puntero al primer **elemento CounterItem agregado.**

Si el carácter comodín daría lugar a un contador duplicado, el error no se notifica y no se crea ningún duplicado. Si se produce una condición de error antes de crear todos los contadores, se notifica el error y no se crean los contadores restantes.

No hay ningún límite en el número de contadores que puede agregar; sin embargo, SYSMON representará solo los primeros 1024 contadores de la colección. No hay ningún límite en el número de contadores que SYSMON mostrará en un informe.

Para recibir una notificación cuando se agrega un contador, implemente [el evento OnCounterAdded.](systemmonitor-oncounteradded.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

