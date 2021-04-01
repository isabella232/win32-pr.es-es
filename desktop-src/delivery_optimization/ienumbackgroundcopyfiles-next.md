---
title: Método Next IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un número especificado de elementos en la secuencia de enumeración. Si hay menos del número solicitado de elementos que quedan en la secuencia, recupera los elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Método Next
- Método siguiente, interfaz IEnumBackgroundCopyFiles
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
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996869"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles:: Next (método)

Recupera un número especificado de elementos en la secuencia de enumeración. Si hay menos del número solicitado de elementos que quedan en la secuencia, recupera los elementos restantes.

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

*Celt* \[ de\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*rgelt* \[ enuncia\]
</dt> <dd>

Matriz de objetos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) . Debe liberar cada objeto en *rgelt* cuando haya terminado.

</dd> <dt>

*pceltFetched* \[ enuncia\]
</dt> <dd>

Número de elementos devueltos en *rgelt*. Puede establecer *pceltFetched* en **null** si *Celt* es uno. De lo contrario, inicialice el valor de *pceltFetched* en 0 antes de llamar a este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El número de elementos solicitados se devolvió correctamente.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Devuelve un valor menor que el número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





