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
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068856"
---
# <a name="counters-collection"></a>Recopilación de contadores

Use esta clase para administrar la colección de [**objetos CounterItem.**](counteritem.md)

Para recuperar este objeto, llame [**a SystemMonitor.Counters**](systemmonitor-counters.md).

## <a name="members"></a>Members

La **colección Counters** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **colección Counters** tiene estos métodos.



| Método                            | Descripción                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Añadir**](counters-add.md)       | Agrega una [**instancia counterItem**](counteritem.md) a la colección.<br/>      |
| [**Remove**](counters-remove.md) | Quita una [**instancia counterItem**](counteritem.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La **colección Counters** tiene estas propiedades.



| Propiedad                                   | Descripción                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contar**](counters-count.md)<br/> | Recupera el número de [**instancias CounterItem**](counteritem.md) de la colección.<br/>  |
| [**Elemento**](counters-item.md)<br/>   | Recupera la instancia de [**CounterItem especificada**](counteritem.md) de la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

El **objeto Counters** es la propiedad predeterminada del [**objeto SystemMonitor.**](systemmonitor.md)

Agregue a esta colección los contadores que desea representar como gráficos. SYSMON recupera los valores del contador del sistema o de un archivo de registro en función del origen [**de datos**](systemmonitor-datasourcetype.md) que especifique.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





