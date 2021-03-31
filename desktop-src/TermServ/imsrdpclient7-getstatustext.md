---
title: Método IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera el texto de estado para el código de estado especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Método GetStatusText Servicios de Escritorio remoto
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método GetStatusText
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
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802756"
---
# <a name="imsrdpclient7getstatustext-method"></a>IMsRdpClient7:: GetStatusText (método)

Recupera el texto de estado para el código de estado especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StatusCode* \[ de\]
</dt> <dd>

Un **uint** que especifica el código de estado para el que se va a recuperar el texto.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Dirección de un **BSTR** que recibe el texto de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>OpenService. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





