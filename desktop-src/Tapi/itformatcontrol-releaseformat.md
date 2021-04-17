---
description: El método ReleaseFormat libera la estructura asociada con el formato.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'ITFormatControl:: ReleaseFormat (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690534"
---
# <a name="itformatcontrolreleaseformat-method"></a>ITFormatControl:: ReleaseFormat (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **ReleaseFormat** libera la estructura asociada con el formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* \[ de\]
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

 

 




