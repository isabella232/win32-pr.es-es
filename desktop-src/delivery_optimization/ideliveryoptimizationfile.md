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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964000"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interfaz IDeliveryOptimizationFile

Implemente **la interfaz IDeliveryOptimizationFile** para identificar el estado de un archivo específico.

## <a name="members"></a>Members

La **interfaz IDeliveryOptimizationFile** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationFile** tiene estos métodos.



| Método                                                 | Descripción                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Devuelve estadísticas de descarga y carga de un archivo específico.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]                                   |
| Servidor mínimo compatible      | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                               |
| Encabezado                        | Deliveryoptimization.h                                                           |
| IDL                           | DeliveryOptimization.idl                                                         |
| Biblioteca                       | Dosvc.lib                                                                        |
| Archivo DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2 |
