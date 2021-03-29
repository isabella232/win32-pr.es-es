---
title: Colección counters (Isysmon. h)
description: Utilice esta clase para administrar la colección de objetos de tipo de elemento. Para recuperar este objeto, llame a SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Colección de contadores SysMon
- Colección de contadores SysMon, descripción
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666048"
---
# <a name="counters-collection"></a>Colección de contadores

Utilice esta clase para administrar la colección de objetos de tipo de [**elemento**](counteritem.md) .

Para recuperar este objeto, llame a [**SystemMonitor. counters**](systemmonitor-counters.md).

## <a name="members"></a>Miembros

La colección **counters** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La colección **counters** tiene estos métodos.



| Método                            | Descripción                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**Agréguela**](counters-add.md)       | Agrega una instancia de un [**elemento de objeto**](counteritem.md) a la colección.<br/>      |
| [**Retirar**](counters-remove.md) | Quita una instancia de un [**objeto**](counteritem.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La colección **counters** tiene estas propiedades.



| Propiedad                                   | Descripción                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contabiliza**](counters-count.md)<br/> | Recupera el número de instancias de los [**Contraelementos**](counteritem.md) de la colección.<br/>  |
| [**Elemento**](counters-item.md)<br/>   | Recupera la instancia de un [**elemento de objeto**](counteritem.md) especificado de la colección.<br/> |



 

## <a name="remarks"></a>Observaciones

El objeto **counters** es la propiedad predeterminada del objeto [**SystemMonitor**](systemmonitor.md) .

Agregue a esta colección los contadores que desea representar en un gráfico. SYSMON recupera los valores del contador desde el sistema o desde un archivo de registro, en función del [**origen de datos**](systemmonitor-datasourcetype.md) que especifique.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





