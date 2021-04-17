---
description: El método GetNumberOfCapabilities recupera el número de funciones asociadas al formato actual.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl:: GetNumberOfCapabilities (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690536"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>ITFormatControl:: GetNumberOfCapabilities (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetNumberOfCapabilities** recupera el número de funciones asociadas al formato actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwCount* \[ enuncia\]
</dt> <dd>

Recuento de las capacidades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




