---
title: Interfaz IDeliveryOptimizationFile
description: Implemente la interfaz IDeliveryOptimizationFile para identificar el estado de un archivo específico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interfaz IDeliveryOptimizationFile
- Interfaz IDeliveryOptimizationFile, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714569"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interfaz IDeliveryOptimizationFile

Implemente la interfaz **IDeliveryOptimizationFile** para identificar el estado de un archivo específico.

## <a name="members"></a>Miembros

La interfaz **IDeliveryOptimizationFile** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDeliveryOptimizationFile** tiene estos métodos.



| Método                                                 | Descripción                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**Getstats (**](ideliveryoptimizationfile-getstats.md) | Devuelve las estadísticas de descarga y carga de un archivo específico.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]                                   |
| Servidor mínimo compatible      | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]                               |
| Encabezado                        | Deliveryoptimization. h                                                           |
| IDL                           | DeliveryOptimization. idl                                                         |
| Biblioteca                       | Dosvc. lib                                                                        |
| Archivo DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2 |
