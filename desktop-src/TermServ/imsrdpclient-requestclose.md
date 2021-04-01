---
title: IMsRdpClient RequestClose, método
description: Solicita un cierre estable del control ActiveX Escritorio remoto.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Método RequestClose Servicios de Escritorio remoto
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método RequestClose
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801580"
---
# <a name="imsrdpclientrequestclose-method"></a>IMsRdpClient:: RequestClose (método)

Solicita un cierre estable del control ActiveX Escritorio remoto. Un cierre estable puede incluir la finalización de la sesión de Servicios de Escritorio remoto del usuario, pero no apaga el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCloseStatus* \[ enuncia\]
</dt> <dd>

Valor de la enumeración [**ControlCloseStatus**](controlclosestatus.md) que indica si la aplicación puede cerrar el control inmediatamente. A continuación se muestra una lista de los valores posibles.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

La aplicación contenedora puede continuar para cerrar el control inmediatamente. Este valor también puede indicar que la conexión ya ha finalizado.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

La aplicación contenedora no debe cerrar el control inmediatamente; la aplicación debe esperar a que se produzca uno de los eventos descritos en la siguiente sección de comentarios antes de cerrar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Si el parámetro *pCloseStatus* es igual a **controlCloseWaitForEvents**, la aplicación debe esperar a que se produzca uno de los siguientes eventos antes de que la aplicación cierre el control:

-   [**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md). Si el usuario no ha iniciado sesión en la sesión de Servicios de Escritorio remoto, la aplicación puede llamar a la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y, a continuación, cerrar el control.
-   [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md). Si el usuario ha iniciado sesión en la sesión de Servicios de Escritorio remoto, el control activa un evento **OnConfirmClose** . Este evento permite a la aplicación preguntar al usuario si desea cerrar la conexión. Si el usuario responde afirmativamente al mensaje, la aplicación contenedora puede llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y cerrar el control.

**RequestClose** permite a una aplicación contenedora preguntar al usuario si desea cerrar una conexión. Para obtener más información, vea [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Vea también

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

[**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

