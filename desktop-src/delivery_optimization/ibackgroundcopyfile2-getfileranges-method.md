---
title: Método IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
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
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422240"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2:: GetFileRanges (método)

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

Número de elementos de *intervalos*.

</dd> <dt>

*Intervalos* \[ de enuncia\]
</dt> <dd>

Matriz de estructuras [**BG_FILE_RANGE**](bg-file-range.md) que especifican los intervalos que se van a descargar. Cuando haya terminado, llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *intervalos*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores devueltos, así como otros.



| Código devuelto                                                                              | Descripción                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Correcto<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | No se especificó ningún intervalo o el trabajo es un trabajo de carga o de carga-respuesta. *RangeCount* se establece en cero y *Ranges* se establece en **null**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 se define como 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

