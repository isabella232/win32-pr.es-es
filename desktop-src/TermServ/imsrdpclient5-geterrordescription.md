---
title: IMsRdpClient5 GetErrorDescription, método
description: Recupera la descripción del error para los eventos de desconexión de la sesión.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Método GetErrorDescription Servicios de Escritorio remoto
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422571"
---
# <a name="imsrdpclient5geterrordescription-method"></a>IMsRdpClient5:: GetErrorDescription (método)

Recupera la descripción del error para los eventos de desconexión de la sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*disconnectReason* \[ de\]
</dt> <dd>

Motivo de la desconexión.

</dd> <dt>

*extendedDisconnectReason* \[ de\]
</dt> <dd>

Proporciona información detallada sobre por qué se inició una desconexión.

</dd> <dt>

*pBstrErrorMsg* \[ enuncia\]
</dt> <dd>

Puntero a una variable **BSTR** que recibe el texto del mensaje de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 se define como 4eb5335b-6429-477d-B922-e06a28ecd8bf<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

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

 

 





