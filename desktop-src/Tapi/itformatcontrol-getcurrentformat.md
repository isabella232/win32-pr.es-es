---
description: El método GetCurrentFormat recupera el formato de medios de la secuencia actual.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'ITFormatControl:: GetCurrentFormat (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690537"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>ITFormatControl:: GetCurrentFormat (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetCurrentFormat** recupera el formato de medios de la secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMediaType* \[ enuncia\]
</dt> <dd>

Puntero a un descriptor de **\_ \_ tipo de medio am** del formato de terminal. Para obtener más información sobre el **\_ \_ tipo de medio am**, consulte la documentación de DirectX.

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

 

 




