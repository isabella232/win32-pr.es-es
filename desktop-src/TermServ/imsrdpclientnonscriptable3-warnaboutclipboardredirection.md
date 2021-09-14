---
title: Propiedad IMsRdpClientNonScriptable3 WarnAboutClipboardRedirection
description: Especifica o recupera si se debe mostrar el cuadro de diálogo advertencia de seguridad para advertir a los usuarios sobre el redireccionamiento del Portapapeles.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , objeto MsRdpClient5
- Objeto MsRdpClient5 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068628"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>Propiedad IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection

Especifica o recupera si se debe mostrar el cuadro de diálogo advertencia de seguridad para advertir a los usuarios sobre el redireccionamiento del Portapapeles.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si se debe mostrar el cuadro de diálogo advertencia de seguridad para advertir a los usuarios sobre el redireccionamiento del Portapapeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





