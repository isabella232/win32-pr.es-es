---
title: IDeliveryOptimizationFile (interfaz)
description: Implemente la interfaz IDeliveryOptimizationFile para identificar el estado de un archivo específico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- IDeliveryOptimizationFile (interfaz)
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
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635745"
---
# <a name="ideliveryoptimizationfile-interface"></a>IDeliveryOptimizationFile (interfaz)

Implemente **la interfaz IDeliveryOptimizationFile** para identificar el estado de un archivo específico.

## <a name="members"></a>Miembros

La **interfaz IDeliveryOptimizationFile** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationFile** tiene estos métodos.



| Método                                                 | Descripción                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Devuelve estadísticas de descarga y carga para un archivo específico.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]                                   |
| Servidor mínimo compatible      | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                               |
| Header                        | Deliveryoptimization.h                                                           |
| Idl                           | DeliveryOptimization.idl                                                         |
| Biblioteca                       | Dosvc.lib                                                                        |
| Archivo DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2 |
