---
title: Propiedad EnableCredSspSupport de IMsRdpClientNonScriptable3
description: Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , objeto MsRdpClient5
- Objeto MsRdpClient5 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f682fe85de22bcffad42d5da80c2f565f4690373629a804c7bbb4fefafa23b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125695"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a>Propiedad IMsRdpClientNonScriptable3::EnableCredSspSupport

Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si CredSSP está habilitado para esta conexión.

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

 

 





