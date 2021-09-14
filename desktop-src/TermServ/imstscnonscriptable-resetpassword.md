---
title: Método ResetPassword de IMsTscNonScriptable
description: Restablece todos los estados de contraseña en el Escritorio remoto ActiveX control .
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Método ResetPassword Servicios de Escritorio remoto
- Método ResetPassword Servicios de Escritorio remoto , interfaz IMsTscNonScriptable
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto método , ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160591"
---
# <a name="imstscnonscriptableresetpassword-method"></a>IMsTscNonScriptable::ResetPassword (método)

Restablece todos los estados de contraseña en el Escritorio remoto ActiveX control . Puede llamar a este método para borrar las contraseñas almacenadas en cualquiera de los tres formatos admitidos: texto no cifrado, codificado portable o binario (noportable). Tenga en cuenta que las contraseñas codificadas no deben considerarse cifradas de forma segura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

Puede llamar a este método para restablecer la contraseña del control después de desconectarse. Esto garantiza que las conexiones posteriores que usan la misma instancia del control no inicien sesión automáticamente con una contraseña establecida previamente.

Solo puede llamar a este método cuando el control Escritorio remoto ActiveX no está en el estado conectado. Este método devuelve **E \_ FAIL si** se llama cuando el control está conectado. Para comprobar el estado conectado, llame al método [**get \_ Connected**](imstscax-connected.md) a través de la interfaz [**IMsTscAx**](imstscax-interface.md) o una de las interfaces que hereda de ella.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





