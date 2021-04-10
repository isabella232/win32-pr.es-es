---
title: IMsTscAxEvents OnConfirmClose, método
description: Se llama cuando el cliente llama al método RequestClose de IMsRdpClient.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Método OnConfirmClose Servicios de Escritorio remoto
- Método OnConfirmClose Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151221"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>IMsTscAxEvents:: OnConfirmClose (método)

Se llama cuando el cliente llama al método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) . En respuesta a este evento, se debe solicitar al usuario que confirme el cierre de la conexión. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

## <a name="syntax"></a>Sintaxis


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfAllowClose* \[ enuncia\]
</dt> <dd>

Si **Variant \_ es true**, el valor predeterminado indica que el usuario desea cerrar la conexión. Si la **variante \_ es falsa**, indica que el usuario no desea cerrar la conexión. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando una aplicación contenedora llama al método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , este método devuelve un valor que indica si el contenedor debe esperar a que se produzca un evento **OnConfirmClose** antes de cerrar la conexión de control. Si **RequestClose** devuelve **controlCloseWaitForEvents** y el usuario está conectado e iniciado sesión en su servicios de escritorio remoto sesión, se desencadena el evento **OnConfirmClose** . En ese momento, la aplicación contenedora puede preguntar al usuario, preguntando si el usuario desea cerrar la conexión. Si el usuario desea cerrar la conexión, la aplicación debe establecer el parámetro *pfAllowClose* en **Variant \_ true** y continuar con el cierre de la conexión. Si el usuario no desea cerrar, la aplicación debe establecer *pfAllowClose* en **Variant \_ false** y dejar la conexión abierta.

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

 

 





