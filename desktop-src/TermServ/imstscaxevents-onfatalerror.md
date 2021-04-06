---
title: IMsTscAxEvents OnFatalError, método
description: Se llama cuando el control de cliente encuentra un error irrecuperable.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Método OnFatalError Servicios de Escritorio remoto
- Método OnFatalError Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnFatalError
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
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905382"
---
# <a name="imstscaxeventsonfatalerror-method"></a>IMsTscAxEvents:: OnFatalError (método)

Se llama cuando el control de cliente encuentra un error irrecuperable.

## <a name="syntax"></a>Sintaxis


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ErrorCode* \[ de\]
</dt> <dd>

Indica el código de error.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


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

Error de memoria insuficiente.

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

Código de error interno 3. No es un estado válido.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**1,8**


</dt> <dd>

Código de error 4 interno.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7**


</dt> <dd>

Se ha producido un error irrecuperable durante la conexión del cliente.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Error de inicialización de Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En respuesta a este evento, el contenedor muestra un mensaje de error y se cierra.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





