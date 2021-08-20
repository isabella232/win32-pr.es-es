---
title: Interfaz IDeliveryOptimizationJob2
description: Más información sobre la interfaz IDeliveryOptimizationJob2
keywords:
- Interfaz IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4960b754d70aa8ff16e60fc8614fba455f57768caa261d3b50c8c78093919626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811148"
---
# <a name="ideliveryoptimizationjob2-interface"></a>Interfaz IDeliveryOptimizationJob2

IDeliveryOptimizationJob2 permite agregar un único archivo al trabajo de descarga y recuperar el archivo inmediatamente. Esta interfaz también admite la configuración y obtención de propiedades de trabajo opcionales.

## <a name="members"></a>Miembros

La **interfaz IDeliveryOptimizationJob2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationJob2** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationJob2** tiene estos métodos.

| Método                                              | Descripción                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | El método AddFile agrega un único archivo a un trabajo de DO existente.         |
| [**Getproperty**](ideliveryoptimizationjob2-getproperty.md) | El método AddFile agrega un único archivo a un trabajo de DO existente. |
| [**Setproperty**](ideliveryoptimizationjob2-setproperty.md) | Este método no se usa.                                       |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                   |
| Servidor mínimo compatible | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                               |
| Header                   | Deliveryoptimization.h                                                           |
| Idl                      | DeliveryOptimization.idl                                                         |
| Biblioteca                  | Dosvc.lib                                                                        |
| Archivo DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4MIENTO-9F8B-D5092D5A2405 |
