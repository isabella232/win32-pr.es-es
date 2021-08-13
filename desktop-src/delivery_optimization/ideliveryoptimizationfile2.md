---
title: Interfaz IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 admite la configuración y obtención de propiedades de archivo opcionales.
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
ms.openlocfilehash: ed7409635444885b662688ce94c300aae6e62186dd76bd7278b3e7445ef50c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542050"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interfaz IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** admite la configuración y obtención de propiedades de archivo opcionales. 

## <a name="members"></a>Miembros

La **interfaz IDeliveryOptimizationFile2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile2** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationFile2** tiene estos métodos.

| Método                                                 | Descripción                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**Getproperty**](ideliveryoptimizationfile2-getproperty.md)  | Este método devuelve una sola propiedad del archivo DO. |
| [**Setproperty**](ideliveryoptimizationfile2-setproperty.md)  | Este método establece una sola propiedad del archivo DO.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                    |
| Servidor mínimo compatible      | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                                |
| Header                        | Deliveryoptimization.h                                                            |
| Idl                           | DeliveryOptimization.idl                                                          |
| Biblioteca                       | Dosvc.lib                                                                         |
| Archivo DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 se define como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
