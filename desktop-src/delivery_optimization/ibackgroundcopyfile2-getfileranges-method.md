---
title: Método IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization.h)
description: Recupera los intervalos que desea descargar del archivo remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Método GetFileRanges
- Método GetFileRanges, interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, método GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047083"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2::GetFileRanges (método)

Recupera los intervalos que desea descargar del archivo remoto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RangeCount* \[ in, out\]
</dt> <dd>

Número de elementos de *ranges.*

</dd> <dt>

*Intervalos* \[ out\]
</dt> <dd>

Matriz de [**BG_FILE_RANGE**](bg-file-range.md) que especifican los intervalos que se van a descargar. Cuando haya terminado, llame a [**la función CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *intervalos*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos, así como otros.



| Código devuelto                                                                              | Descripción                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Success<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | No se especificó ningún intervalo o el trabajo es un trabajo de carga o carga-respuesta. *RangeCount* se establece en cero y *Ranges* en **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 se define como 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

