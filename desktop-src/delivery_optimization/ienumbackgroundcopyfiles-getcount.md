---
title: Método GetCount de IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Recupera un recuento del número de archivos de la enumeración .
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (método)
- Método GetCount, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67ee932079a7c67619fe769cbe5d1b6705261655853f1adccb14bf5d12eecf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409915"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>IEnumBackgroundCopyFiles::GetCount (método)

Recupera un recuento del número de archivos de la enumeración .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCount* \[ out\]
</dt> <dd>

Número de archivos de la enumeración .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** correcto o uno de los valores **HRESULT** COM estándar en caso de error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





