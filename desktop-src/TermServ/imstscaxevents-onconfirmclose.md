---
title: Método OnConfirmClose de IMsTscAxEvents
description: Se llama cuando el cliente llama al método IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Método OnConfirmClose Servicios de Escritorio remoto
- Método OnConfirmClose Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnConfirmClose
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968223"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>IMsTscAxEvents::OnConfirmClose (método)

Se llama cuando el cliente llama [**al método IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md) En respuesta a este evento, se debe solicitar al usuario que confirme el cierre de la conexión. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

## <a name="syntax"></a>Sintaxis


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfAllowClose* \[ out\]
</dt> <dd>

Si **VARIANT \_ TRUE** es , el valor predeterminado indica que el usuario desea cerrar la conexión. Si **VARIANT \_ FALSE** indica que el usuario no desea cerrar la conexión. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando una aplicación contenedora llama al método [**IMsRdpClient::RequestClose,**](imsrdpclient-requestclose.md) ese método devuelve un valor que indica si el contenedor debe esperar a que se produzca un evento **OnConfirmClose** antes de cerrar la conexión de control. Si **RequestClose** devuelve **controlCloseWaitForEvents** y el usuario está conectado y ha iniciado sesión en su sesión Servicios de Escritorio remoto sesión, se activa el evento **OnConfirmClose.** En ese momento, la aplicación contenedora puede preguntar al usuario si quiere cerrar la conexión. Si el usuario desea cerrar la conexión, la aplicación debe establecer el *parámetro pfAllowClose* en **VARIANT \_ TRUE** y continuar con el cierre de la conexión. Si el usuario no desea cerrar, la aplicación debe establecer *pfAllowClose* en **VARIANT \_ FALSE** y dejar abierta la conexión.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





