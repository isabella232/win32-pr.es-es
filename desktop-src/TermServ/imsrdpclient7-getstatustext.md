---
title: Método IMsRdpClient7 GetStatusText (Openservice.h)
description: Recupera el texto de estado del código de estado especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Método GetStatusText Servicios de Escritorio remoto
- Método GetStatusText Servicios de Escritorio remoto interfaz , IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto método , GetStatusText
- Método GetStatusText Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto método , GetStatusText
- Método GetStatusText Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto método , GetStatusText
- Método GetStatusText Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto método , GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285195"
---
# <a name="imsrdpclient7getstatustext-method"></a>IMsRdpClient7::GetStatusText (método)

Recupera el texto de estado del código de estado especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*statusCode* \[ En\]
</dt> <dd>

UINT **que** especifica el código de estado para el que se recuperará el texto.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Dirección de un **BSTR** que recibe el texto de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Openservice.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID IMsRdpClient7 se define como \_ b2a5b5ce-3461-444a-91d4-add26d070638<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





