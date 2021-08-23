---
title: Método Skip de IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Omite el siguiente número especificado de elementos en la secuencia de enumeración. Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, omite el último elemento de la secuencia.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (método)
- Método Skip, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método Skip
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 174b8ac3e0286a4d2a19e211773969d408c7f7762e8b2dd4fe743f0b4b2aabeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567365"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>IEnumBackgroundCopyFiles::Skip (Método)

Omite el siguiente número especificado de elementos en la secuencia de enumeración. Si quedan menos elementos en la secuencia que el número solicitado de elementos que se van a omitir, omite el último elemento de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Omitió correctamente el número de elementos solicitados.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Se omite menos que el número de elementos solicitados.<br/>    |



 

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





