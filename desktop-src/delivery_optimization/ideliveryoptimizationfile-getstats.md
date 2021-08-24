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
ms.openlocfilehash: f4e2f0a3b680e682944740cb570bfb4889b22ba8e7ec56d3aefc9e34fcdd6a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635765"
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
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





