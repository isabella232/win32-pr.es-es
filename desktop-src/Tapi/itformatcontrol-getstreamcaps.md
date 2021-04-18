---
description: El método GetStreamCaps recupera las capacidades asociadas a un índice de formato determinado.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl:: GetStreamCaps (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690535"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>ITFormatControl:: GetStreamCaps (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetStreamCaps** recupera las capacidades asociadas a un índice de formato determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Índice del formato que se va a sondear.

</dd> <dt>

*ppMediaType* \[ enuncia\]
</dt> <dd>

Puntero a un descriptor de **\_ \_ tipo de medio am** del formato de terminal. Para obtener más información sobre el **\_ \_ tipo de medio am**, consulte la documentación de DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ enuncia\]
</dt> <dd>

Una estructura de [**configuración de secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) que proporciona información detallada sobre las capacidades de streaming.

</dd> <dt>

*pfEnabled* \[ enuncia\]
</dt> <dd>

Indica si el formato asociado al índice actual está habilitado.

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
</dt> <dt>

[**\_Cap de \_ configuración de secuencia TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




