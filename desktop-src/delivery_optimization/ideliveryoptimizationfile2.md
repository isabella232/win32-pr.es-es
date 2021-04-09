---
title: Interfaz IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 admite el establecimiento y la obtención de propiedades de archivo opcionales.
keywords:
- Interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079141"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interfaz IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** admite el establecimiento y la obtención de propiedades de archivo opcionales. 

## <a name="members"></a>Miembros

La interfaz **IDeliveryOptimizationFile2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile2** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDeliveryOptimizationFile2** tiene estos métodos.

| Método                                                 | Descripción                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Este método devuelve una única propiedad del archivo DO. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Este método establece una propiedad única del archivo DO.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]                                    |
| Servidor mínimo compatible      | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]                                |
| Encabezado                        | Deliveryoptimization. h                                                            |
| IDL                           | DeliveryOptimization. idl                                                          |
| Biblioteca                       | Dosvc. lib                                                                         |
| Archivo DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 se define como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
