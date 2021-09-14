---
title: Interfaz IDeliveryOptimizationJob (Deliveryoptimization.h)
description: Use la interfaz IDeliveryOptimizationJob para descargar intervalos de un archivo.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interfaz IDeliveryOptimizationJob
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
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970095"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interfaz IDeliveryOptimizationJob

Use la **interfaz IDeliveryOptimizationJob** para descargar intervalos de un archivo.

## <a name="members"></a>Members

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
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

