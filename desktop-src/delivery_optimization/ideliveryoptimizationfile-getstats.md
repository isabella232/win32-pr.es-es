---
title: Método IDeliveryOptimizationFile Getstats ((Deliveryoptimization. h)
description: Devuelve las estadísticas de descarga y carga de un archivo específico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (método)
- Método Getstats (, interfaz IDeliveryOptimizationFile
- Interfaz IDeliveryOptimizationFile, método Getstats (
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422528"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>IDeliveryOptimizationFile:: Getstats ((método)

Devuelve las estadísticas de descarga y carga de un archivo específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*swarmStats* \[ enuncia\]
</dt> <dd>

Devuelve las estadísticas de descarga y carga de un archivo específico. Para obtener más información, vea la estructura [**DOSwarmStats**](doswarmstats.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver **S_OK**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





