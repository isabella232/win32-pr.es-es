---
description: Especifica si un trabajo de impresión XPS está en la fase de puesta en cola o en la fase de representación.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumeración EPrintXPSJobOperation (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813547"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Enumeración EPrintXPSJobOperation

Especifica si un trabajo de impresión XPS está en la fase de puesta en cola o en la fase de representación.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

El trabajo XPS está en cola.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

El trabajo XPS se está representando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa principalmente como parámetro para la función [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



 

 




