---
title: Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession
description: Devuelve una referencia a un enumerador de punto de conexión de audio para el ID. de sesión especificado.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto función de devolución de llamada GetTSAudioEndpointEnumeratorForSession
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686177"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Función de devolución de llamada GetTSAudioEndpointEnumeratorForSession

Devuelve una referencia a un enumerador de punto de conexión de audio para el ID. de sesión especificado. Los consumidores de este enumerador de punto de conexión de audio, como MMDevAPI.dll, llaman a esta función para recuperar un enumerador de punto de conexión de audio en una sesión de Servicios de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SessionID* \[ de\]
</dt> <dd>

Identificador de la sesión de Servicios de Escritorio remoto.

</dd> <dt>

*ppEndpointEnumerator* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a una interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve **S \_ correcto**.

## <a name="remarks"></a>Observaciones

Esta función no está definida en un archivo de encabezado. Debe implementar y exportar esta función en el enumerador de punto de conexión personalizado y usar la firma que se muestra en el bloque de sintaxis anteriormente en este tema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>         |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Implementación de un enumerador de punto de conexión de audio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

