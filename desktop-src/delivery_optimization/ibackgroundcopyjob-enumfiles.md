---
title: Método IBackgroundCopyJob Enumfiles ((Deliveryoptimization. h)
description: Recupera un puntero de la interfaz IEnumBackgroundCopyFiles que se usa para enumerar los archivos de un trabajo.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método Enumfiles (
- Método Enumfiles (, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Enumfiles (
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150417"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>IBackgroundCopyJob:: Enumfiles ((método)

Recupera un puntero de la interfaz [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos de un trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumFiles* \[ enuncia\]
</dt> <dd>

Puntero de interfaz [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que se usa para enumerar los archivos del trabajo. Suelte *ppEnumFiles* cuando termine.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





