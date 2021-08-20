---
title: IMsRdpClientNonScriptable4 WarnAboutPrinterRedirection, propiedad
description: Controla si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras antes de iniciar una sesión.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto interfaz , IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto propiedad , WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto interfaz , IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto propiedad , WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad WarnAboutPrinterRedirection
- Propiedad WarnAboutPrinterRedirection Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad WarnAboutPrinterRedirection
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
ms.openlocfilehash: b24f3969e32b500c23d52111de0533bd0812a269f8d08d62abfeea14275dbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941166"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a>IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection, propiedad

Controla si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras antes de iniciar una sesión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor de propiedad

Establece si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





