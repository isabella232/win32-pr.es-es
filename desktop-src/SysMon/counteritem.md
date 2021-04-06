---
title: Objeto de contraelemento (Isysmon. h)
description: Utilice esta clase para recuperar la ruta de acceso y el valor de un contador y para especificar el color que se usa para representar el contador. Para recuperar este objeto, llame a Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Objeto de contraelemento SysMon
- Objeto de contraelemento SysMon, descrito
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802587"
---
# <a name="counteritem-object"></a>Objeto de elemento

Utilice esta clase para recuperar la ruta de acceso y el valor de un contador y para especificar el color que se usa para representar el contador.

Para recuperar este objeto, llame a [**Counters. Item**](counters-item.md).

## <a name="members"></a>Miembros

El objeto de tipo de **elemento** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **peritem** tiene estos métodos.



| Método                                             | Descripción                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetDataAt**](counteritem-getdataat.md)         | Recupera los datos del contador de un punto concreto del gráfico de líneas.<br/> |
| [**GetStatistics**](counteritem-getstatistics.md) | Recupera los valores promedio, máximo y mínimo del contador.<br/> |
| [**GetValue**](counteritem-getvalue.md)           | Recupera el último valor del contador.<br/>                            |



 

### <a name="properties"></a>Propiedades

El objeto de **peritem** tiene estas propiedades.



| Propiedad                                                  | Descripción                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Color**](counteritem-color.md)<br/>             | Recupera o establece el color utilizado para representar el valor del contador en el gráfico.<br/>         |
| [**Estilo de línea**](counteritem-linestyle.md)<br/>     | Recupera o establece el estilo de línea que se usa para representar el valor del contador.<br/>    |
| [**Ruta**](counteritem-path.md)<br/>               | Recupera la ruta de acceso del contador.<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | Recupera o establece el factor de escala que se usa para representar el valor del contador.<br/>  |
| [**Seleccionado**](counteritem-selected.md)<br/>       | Recupera o establece un valor que indica si el contador está seleccionado.<br/> |
| [**Value**](counteritem-value.md)<br/>             | Recupera el valor actual del contador.<br/>                          |
| [**Visible**](counteritem-visible.md)<br/>         | Recupera o establece un valor que indica si el contador está gráfico.<br/>  |
| [**Width**](counteritem-width.md)<br/>             | Recupera o establece el ancho de línea que se usa para representar el valor del contador.<br/>    |



 

## <a name="remarks"></a>Observaciones

[**Value**](counteritem-value.md) es la propiedad predeterminada de **peritem**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases SYSMON](sysmon-classes.md)
</dt> </dl>

 

 





