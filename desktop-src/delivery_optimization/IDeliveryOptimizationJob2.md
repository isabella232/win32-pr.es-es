---
title: Interfaz IDeliveryOptimizationJob2
description: 'Más información acerca de: interfaz IDeliveryOptimizationJob2'
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
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714851"
---
# <a name="ideliveryoptimizationjob2-interface"></a>Interfaz IDeliveryOptimizationJob2

IDeliveryOptimizationJob2 permite agregar un solo archivo al trabajo de descarga y recuperar el archivo inmediatamente. Esta interfaz también admite la configuración y la obtención de propiedades de trabajo opcionales.

## <a name="members"></a>Miembros

La interfaz **IDeliveryOptimizationJob2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob2** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDeliveryOptimizationJob2** tiene estos métodos.

| Método                                              | Descripción                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | El método AddFile agrega un solo archivo a un trabajo existente.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | El método AddFile agrega un solo archivo a un trabajo existente. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Este método no se utiliza.                                       |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]                                   |
| Servidor mínimo compatible | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]                               |
| Encabezado                   | Deliveryoptimization. h                                                           |
| IDL                      | DeliveryOptimization. idl                                                         |
| Biblioteca                  | Dosvc. lib                                                                        |
| Archivo DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
