---
title: Método WSMan.GetErrorMessage (WSManDisp.h)
description: Devuelve una cadena con formato que contiene el texto de un número de error.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Método GetErrorMessage Windows administración remota
- Método GetErrorMessage Windows administración remota , objeto WSMan
- Objeto WSMan Windows administración remota, método GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742095"
---
# <a name="wsmangeterrormessage-method"></a>Método WSMan.GetErrorMessage

Devuelve una cadena con formato que contiene el texto de un número de error. Este método realiza la misma operación que la línea de **comandos winrm** **helpmsg** *decimal o hexadecimal número de error*.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*errorNumber* \[ En\]
</dt> <dd>

Número de mensaje de error en formato decimal o hexadecimal de WinRM, WinHTTP u otros componentes del sistema operativo.

</dd> <dt>

*errorMessage* \[ out\]
</dt> <dd>

Cadena de mensaje de error con formato de mensajes devueltos desde el **comando Winrm.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El método de C++ correspondiente [**es IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





