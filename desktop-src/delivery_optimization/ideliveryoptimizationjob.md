---
title: Interfaz IDeliveryOptimizationJob (Deliveryoptimization.h)
description: Use la interfaz IDeliveryOptimizationJob para descargar intervalos de un archivo.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- IDeliveryOptimizationJob (interfaz)
- Interfaz IDeliveryOptimizationJob, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71f978be993e21ad487af5469327b5f66804166a7e5247dffb841f7815b2279e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895685"
---
# <a name="ideliveryoptimizationjob-interface"></a>IDeliveryOptimizationJob (interfaz)

Use la **interfaz IDeliveryOptimizationJob** para descargar intervalos de un archivo.

## <a name="members"></a>Miembros

La **interfaz IDeliveryOptimizationJob** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationJob** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationJob** tiene estos métodos.



| Método                                                                  | Descripción                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

