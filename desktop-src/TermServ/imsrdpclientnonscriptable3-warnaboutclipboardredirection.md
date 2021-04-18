---
title: Propiedad WarnAboutClipboardRedirection de IMsRdpClientNonScriptable3
description: Especifica o recupera si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutClipboardRedirection
- Propiedad WarnAboutClipboardRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutClipboardRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutClipboardRedirection, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutClipboardRedirection
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533933"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>IMsRdpClientNonScriptable3:: WarnAboutClipboardRedirection (propiedad)

Especifica o recupera si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.

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

Especifica si se debe mostrar el cuadro de diálogo Advertencia de seguridad para advertir a los usuarios acerca de la redirección del portapapeles.

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

 

 





