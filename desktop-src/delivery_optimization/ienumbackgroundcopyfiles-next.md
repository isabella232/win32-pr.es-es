---
title: Método IEnumBackgroundCopyFiles Next (Deliveryoptimization.h)
description: Recupera un número especificado de elementos en la secuencia de enumeración. Si quedan menos elementos que el número solicitado de elementos en la secuencia, recupera los elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Método Next
- Método Next, interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, método Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dcf24c65b7f282b1a1e15d3109ce1af9ccfc0af6436c80c94760f0b4cd18069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461885"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles::Next (Método)

Recupera un número especificado de elementos en la secuencia de enumeración. Si quedan menos elementos que el número solicitado de elementos en la secuencia, recupera los elementos restantes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Matriz de [**objetos IBackgroundCopyFile.**](ibackgroundcopyfile.md) Debe liberar cada objeto en *rgelt cuando* haya terminado.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Número de elementos devueltos en *rgelt*. Puede establecer *pceltFetched en* **NULL** si *celt* es uno. De lo contrario, inicialice el *valor de pceltFetched* en 0 antes de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Devolvió correctamente el número de elementos solicitados.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Se devuelve un valor menor que el número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





