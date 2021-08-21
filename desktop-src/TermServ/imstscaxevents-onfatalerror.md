---
title: Método IMsTscAxEvents OnFatalError
description: Se llama cuando el control de cliente encuentra un error grave.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Método OnFatalError Servicios de Escritorio remoto
- Método OnFatalError Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a10315eca4fcbf96edf123699614d29a2c0b8974f563c52148b5de75310fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000685"
---
# <a name="imstscaxeventsonfatalerror-method"></a>IMsTscAxEvents::OnFatalError (método)

Se llama cuando el control de cliente encuentra un error grave.

## <a name="syntax"></a>Sintaxis


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*errorCode* \[ En\]
</dt> <dd>

Indica el código de error.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Se ha producido un error desconocido.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Código de error interno 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Se ha producido un error de memoria fuera de memoria.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Se ha producido un error de creación de ventana.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Código de error interno 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

Código de error interno 3. Este no es un estado válido.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6**


</dt> <dd>

Código de error interno 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Se ha producido un error irrecuperable durante la conexión de cliente.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Error de inicialización de Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

En respuesta a este evento, el contenedor muestra un mensaje de error y se apaga.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





