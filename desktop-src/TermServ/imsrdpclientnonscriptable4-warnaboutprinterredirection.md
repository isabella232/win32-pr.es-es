---
title: Propiedad WarnAboutPrinterRedirection de IMsRdpClientNonScriptable4
description: Controla si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora antes de iniciar una sesión.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutPrinterRedirection
- Servicios de Escritorio remoto de la propiedad WarnAboutPrinterRedirection, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359759"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a>IMsRdpClientNonScriptable4:: WarnAboutPrinterRedirection (propiedad)

Controla si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora antes de iniciar una sesión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor de propiedad

Establece si el cuadro de diálogo de redirección muestra un mensaje sobre la redirección de la impresora.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





