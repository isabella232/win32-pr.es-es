---
description: El método GetStreamCaps recupera las funcionalidades asociadas a un índice de formato determinado.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: Método ITFormatControl::GetStreamCaps (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f54cbd44a946c0fcd3cf297c4cacadc49369765b8c1b6505031a145768c3b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406115"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>ItFormatControl::GetStreamCaps (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetStreamCaps** recupera las funcionalidades asociadas a un índice de formato determinado.

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

*dwIndex* \[ En\]
</dt> <dd>

Índice del formato que se está sondeando.

</dd> <dt>

*ppMediaType* \[ out\]
</dt> <dd>

Puntero a un descriptor **\_ AM MEDIA \_ TYPE** del formato de terminal. Para obtener más información sobre **AM \_ MEDIA \_ TYPE,** consulte la documentación de DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ out\]
</dt> <dd>

Estructura [**TAPI \_ STREAM CONFIG \_ \_ CAPS**](tapi-stream-config-caps.md) que proporciona información detallada sobre las funcionalidades de flujo.

</dd> <dt>

*pfEnabled* \[ out\]
</dt> <dd>

Indica si el formato asociado al índice actual está habilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




