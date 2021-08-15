---
title: Propiedad ConnectionBarText de IMsRdpClientNonScriptable3
description: Establece o recupera el texto para actualizar la barra de conexión.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Propiedad ConnectionBarText Servicios de Escritorio remoto
- Propiedad ConnectionBarText Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , objeto MsRdpClient5
- Objeto MsRdpClient5 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dac8f704f5ecaa7bd521af10f05fd1c56d2adebff70827862478847a782faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941598"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a>Propiedad IMsRdpClientNonScriptable3::ConnectionBarText

Establece o recupera el texto para actualizar la barra de conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la cadena de texto que se mostrará en la barra de conexión.

## <a name="remarks"></a>Comentarios

Debe llamar al método **IMsRdpClientNonScriptable3::p ut \_ ConnectionBarText** antes de llamar al método [**IMsTscSecuredSettings::p ut \_ Fullscreen**](imstscsecuredsettings-fullscreen.md) o al método [**IMsRdpClient::p ut \_ Fullscreen.**](imsrdpclient-fullscreen.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





