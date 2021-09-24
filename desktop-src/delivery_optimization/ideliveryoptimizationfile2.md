---
title: IDeliveryOptimizationFile2 (interfaz)
description: IDeliveryOptimizationFile2 admite la configuración y la obtención de propiedades de archivo opcionales.
keywords:
- IDeliveryOptimizationFile2 (interfaz)
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
ms.openlocfilehash: 7e5ef827758e054ed391303a283b490e0db66d3b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520052"
---
# <a name="ideliveryoptimizationfile2-interface"></a>IDeliveryOptimizationFile2 (interfaz)

**IDeliveryOptimizationFile2** admite la configuración y la obtención de propiedades de archivo opcionales. 

## <a name="members"></a>Miembros

La **interfaz IDeliveryOptimizationFile2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDeliveryOptimizationFile2** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDeliveryOptimizationFile2** tiene estos métodos.

| Método                                                 | Descripción                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**Getproperty**](ideliveryoptimizationfile2-getproperty.md)  | Este método devuelve una única propiedad del Optimización de distribución archivo. |
| [**Setproperty**](ideliveryoptimizationfile2-setproperty.md)  | Este método establece una única propiedad del Optimización de distribución archivo.    |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible      | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]                                    |
| Servidor mínimo compatible      | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]                                |
| Encabezado                        | Deliveryoptimization.h                                                            |
| IDL                           | DeliveryOptimization.idl                                                          |
| Biblioteca                       | Dosvc.lib                                                                         |
| Archivo DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 se define como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
