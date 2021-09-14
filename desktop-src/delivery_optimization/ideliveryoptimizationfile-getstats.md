---
title: Método IDeliveryOptimizationFile GetStats (Deliveryoptimization.h)
description: Devuelve estadísticas de descarga y carga de un archivo específico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (método)
- Método GetStats, interfaz IDeliveryOptimizationFile
- Interfaz IDeliveryOptimizationFile, método GetStats
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964004"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>IDeliveryOptimizationFile::GetStats (método)

Devuelve estadísticas de descarga y carga de un archivo específico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*swarmStats* \[ out\]
</dt> <dd>

Devuelve estadísticas de descarga y carga de un archivo específico. Consulte la [**estructura DOSwarmStats**](doswarmstats.md) para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver **S_OK**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





