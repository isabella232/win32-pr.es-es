---
title: Colección de contadores (Isysmon.h)
description: Use esta clase para administrar la colección de objetos CounterItem. Para recuperar este objeto, llame a SystemMonitor.Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- SysMon de la colección de contadores
- Colección de contadores SysMon , descrito
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8349c1425450491c3fc658f6ac1ac3c5fcf75d3e617a92f6e34b91f2f5802e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883342"
---
# <a name="counters-collection"></a>Recopilación de contadores

Use esta clase para administrar la colección de [**objetos CounterItem.**](counteritem.md)

Para recuperar este objeto, llame [**a SystemMonitor.Counters**](systemmonitor-counters.md).

## <a name="members"></a>Miembros

La **colección Counters** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **colección Counters** tiene estos métodos.



| Método                            | Descripción                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Añadir**](counters-add.md)       | Agrega una [**instancia counterItem**](counteritem.md) a la colección.<br/>      |
| [**Quitar**](counters-remove.md) | Quita una [**instancia counterItem**](counteritem.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La **colección Counters** tiene estas propiedades.



| Propiedad                                   | Descripción                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Count**](counters-count.md)<br/> | Recupera el número de [**instancias CounterItem**](counteritem.md) de la colección.<br/>  |
| [**Elemento**](counters-item.md)<br/>   | Recupera la instancia de [**CounterItem especificada**](counteritem.md) de la colección.<br/> |



 

## <a name="remarks"></a>Comentarios

El **objeto Counters** es la propiedad predeterminada del [**objeto SystemMonitor.**](systemmonitor.md)

Agregue a esta colección los contadores que desea representar como gráficos. SYSMON recupera los valores del contador del sistema o de un archivo de registro en función del origen [**de datos**](systemmonitor-datasourcetype.md) que especifique.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





