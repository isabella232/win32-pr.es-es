---
title: Propiedad FullScreen de IMsRdpClient
description: Determina si el control de cliente está en modo de pantalla completa.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Propiedad FullScreen Servicios de Escritorio remoto
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , propiedad FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e3d2349a4d3b0121b05a3a0424126b754757c1b0b356042a90c28ce9923ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010075"
---
# <a name="imsrdpclientfullscreen-property"></a>IMsRdpClient::FullScreen, propiedad

Determina si el control de cliente está en modo de pantalla completa.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valor de propiedad

**True** para entrar en modo de pantalla completa, **False** para salir del modo de pantalla completa y volver al modo de ventana.

## <a name="error-codes"></a>Códigos de error

Si los métodos se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Comentarios

Puede establecer esta propiedad cuando el control esté conectado.

Debe llamar al método [**IMsRdpClientNonScriptable3::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de llamar al método [**IMsTscSecuredSettings::p ut \_ Fullscreen**](imstscsecuredsettings-fullscreen.md) o al método **IMsRdpClient::p ut \_ Fullscreen.**

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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
</dt> </dl>

 

 





