---
title: IMsTscNonScriptable ResetPassword, método
description: Restablece todos los Estados de contraseña en el control ActiveX Escritorio remoto.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Método ResetPassword Servicios de Escritorio remoto
- Método ResetPassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto, método ResetPassword
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492773"
---
# <a name="imstscnonscriptableresetpassword-method"></a>IMsTscNonScriptable:: ResetPassword (método)

Restablece todos los Estados de contraseña en el control ActiveX Escritorio remoto. Puede llamar a este método para borrar las contraseñas que se almacenan en cualquiera de los tres formatos admitidos: texto sin formato, codificado de forma portátil o binario (no portable). Tenga en cuenta que las contraseñas codificadas no se deben considerar cifradas de forma segura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Puede llamar a este método para restablecer la contraseña del control después de desconectarse. Esto garantiza que las conexiones posteriores que utilicen la misma instancia del control no inicien sesión automáticamente con una contraseña establecida previamente.

Solo puede llamar a este método cuando el control ActiveX Escritorio remoto no está en estado conectado. Este método devuelve **E \_ FAIL** si se le llama cuando el control está conectado. Para comprobar el estado de conexión, llame al método [**Get \_ Connected**](imstscax-connected.md) a través de la interfaz [**IMsTscAx**](imstscax-interface.md) o una de las interfaces que hereda de él.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





