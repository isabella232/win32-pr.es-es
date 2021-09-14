---
title: Método IMsRdpClient RequestClose
description: Solicita un cierre correcto del control de Escritorio remoto ActiveX.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Método RequestClose Servicios de Escritorio remoto
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , método RequestClose
- Método RequestClose Servicios de Escritorio remoto , interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , método RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890996"
---
# <a name="imsrdpclientrequestclose-method"></a>IMsRdpClient::RequestClose (Método)

Solicita un cierre correcto del control de Escritorio remoto ActiveX. Un cierre estable puede incluir finalizar la sesión de Servicios de Escritorio remoto del usuario, pero no apaga el servidor Escritorio remoto session host (host de sesión de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCloseStatus* \[ out\]
</dt> <dd>

Valor de la [**enumeración ControlCloseStatus**](controlclosestatus.md) que indica si la aplicación puede cerrar el control inmediatamente. A continuación se muestra una lista de valores posibles.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

La aplicación contenedora puede continuar para cerrar el control inmediatamente. Este valor también puede indicar que la conexión ya ha finalizado.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

La aplicación contenedora no debe cerrar el control inmediatamente; La aplicación debe esperar a que uno de los eventos descritos en la sección Comentarios siguiente se produzca antes de cerrarse.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

Si el *parámetro pCloseStatus* es igual a **controlCloseWaitForEvents**, la aplicación debe esperar a que se produzca uno de los siguientes eventos antes de que la aplicación cierre el control:

-   [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md). Si el usuario no ha iniciado sesión en la sesión Servicios de Escritorio remoto, la aplicación puede llamar a la [**función DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y, a continuación, cerrar el control.
-   [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md). Si el usuario ha iniciado sesión en Servicios de Escritorio remoto sesión, el control activa un **evento OnConfirmClose.** Este evento permite a la aplicación preguntar al usuario si desea cerrar la conexión. Si el usuario responde sí al símbolo del sistema, la aplicación contenedora puede llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y cerrar el control.

**RequestClose** permite que una aplicación contenedora solicite al usuario si desea cerrar una conexión. Para obtener más información, [**vea IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

