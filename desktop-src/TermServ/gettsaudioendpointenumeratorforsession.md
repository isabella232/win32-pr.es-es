---
title: Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession
description: Devuelve una referencia a un enumerador de extremo de audio para el identificador de sesión especificado.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f64af1d7e886b418ac87cd360302101a60d746d707652f605a648e9812a5547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059593"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession

Devuelve una referencia a un enumerador de extremo de audio para el identificador de sesión especificado. Los consumidores de este enumerador de extremo de audio, como MMDevAPI.dll, llaman a esta función para recuperar un enumerador de punto de conexión de audio en una Servicios de Escritorio remoto sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SessionId* \[ En\]
</dt> <dd>

Identificador de la Servicios de Escritorio remoto sesión.

</dd> <dt>

*ppEndpointEnumerator* \[ out\]
</dt> <dd>

Dirección de un puntero a una [**interfaz IMMDeviceEnumerator.**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK**.

## <a name="remarks"></a>Comentarios

Esta función no está definida en un archivo de encabezado. Debe implementar y exportar esta función en el enumerador de punto de conexión personalizado y usar la firma que se muestra en el bloque de sintaxis anterior en este tema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Implementar un enumerador de extremo de audio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

