---
title: Método IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: La optimización de entrega (DO) llama a la implementación del método JobModification cuando se ha modificado el trabajo.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Método JobModification
- Método JobModification, interfaz IBackgroundCopyCallback
- Interfaz IBackgroundCopyCallback, método JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714576"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>IBackgroundCopyCallback:: JobModification (método)

La optimización de entrega (DO) llama a la implementación del método [**JobModification**](https://www.bing.com/search?q=**JobModification**) cuando se ha modificado el trabajo. El servicio genera este evento cuando se transfieren bytes, se han agregado archivos al trabajo, se han modificado las propiedades o el estado del trabajo ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJob* \[ de\]
</dt> <dd>

Contiene los métodos para tener acceso a la información de la propiedad, el progreso y el estado del trabajo. No libere *pJob*; Libera la interfaz cuando el método [**JobModification**](https://www.bing.com/search?q=**JobModification**) devuelve.

</dd> <dt>

*dwReserved* \[ de\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método debe devolver S_OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





