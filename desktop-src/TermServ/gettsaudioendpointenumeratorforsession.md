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
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374746"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession

Devuelve una referencia a un enumerador de extremo de audio para el identificador de sesión especificado. Los consumidores de este enumerador de punto de conexión de audio, como MMDevAPI.dll, llaman a esta función para recuperar un enumerador de punto de conexión de audio en una Servicios de Escritorio remoto sesión.

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

## <a name="remarks"></a>Observaciones

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

 

