---
title: Función MpManagerOpen (MpClient.h)
description: Establece una conexión con el administrador de protección contra malware en el equipo local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Función MpManagerOpen Características heredadas del Windows entorno
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324d013c46777ac48af32e6c91f557b7feda3a03fbdf0c21a7c79e8cf5e3d9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883370"
---
# <a name="mpmanageropen-function"></a>Función MpManagerOpen

Establece una conexión con el administrador de protección contra malware en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwReserved* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Reservado para uso futuro. Se debe establecer en 0.

</dd> <dt>

*phMpHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Controlar la interfaz del administrador de protección contra malware. Este identificador debe cerrarse con la [**función MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**. Se garantiza que esta llamada de función se realiza correctamente aunque no se esté ejecutando un servicio AntiMalware.

Si se produce un error en la función, el valor devuelto es un **código HRESULT con** errores. El autor de la llamada puede usar [**la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





