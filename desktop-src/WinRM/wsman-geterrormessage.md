---
title: Método WSMan. GetErrorMessage (WSManDisp. h)
description: Devuelve una cadena con formato que contiene el texto de un número de error.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Método GetErrorMessage Administración remota de Windows
- Administración remota de Windows método GetErrorMessage, objeto WSMan
- Administración remota de Windows de objeto WSMan, método GetErrorMessage
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
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359737"
---
# <a name="wsmangeterrormessage-method"></a>WSMan. GetErrorMessage (método)

Devuelve una cadena con formato que contiene el texto de un número de error. Este método **realiza la misma** operación que la línea de comandos WinRM **HELPMSG** *decimal o el número de error hexadecimal*.

## <a name="syntax"></a>Sintaxis


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*númeroerror* \[ de\]
</dt> <dd>

Un número de mensaje de error en formato decimal o hexadecimal de WinRM, WinHTTP u otros componentes del sistema operativo.

</dd> <dt>

*errorMessage* \[ enuncia\]
</dt> <dd>

Una cadena de mensaje de error con formato de mensajes devueltos por el comando **WinRM** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método de C++ correspondiente es [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





