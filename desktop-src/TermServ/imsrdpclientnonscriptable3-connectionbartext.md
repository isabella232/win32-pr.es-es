---
title: Propiedad ConnectionBarText de IMsRdpClientNonScriptable3
description: Establece o recupera el texto para actualizar la barra de conexión.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad ConnectionBarText
- Propiedad ConnectionBarText Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad ConnectionBarText
- Servicios de Escritorio remoto de la propiedad ConnectionBarText, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad ConnectionBarText
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
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803620"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a>IMsRdpClientNonScriptable3:: ConnectionBarText (propiedad)

Establece o recupera el texto para actualizar la barra de conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la cadena de texto que se va a mostrar en la barra de conexión.

## <a name="remarks"></a>Observaciones

Debe llamar al método **IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText** antes de llamar al método de [**\_ pantalla completa IMsTscSecuredSettings::p UT**](imstscsecuredsettings-fullscreen.md) o al método de [**\_ pantalla completa IMsRdpClient::p UT**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





