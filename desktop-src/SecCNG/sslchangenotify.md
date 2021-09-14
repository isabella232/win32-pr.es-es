---
description: No implementado y no se puede usar.
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: Función SslChangeNotify (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5539ef2529a4f3af86d34ae0e9d44cd31a8f4289
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073644"
---
# <a name="sslchangenotify-function"></a>Función SslChangeNotify

La **función SslChangeNotify** no se implementa y no se puede usar.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **NTE \_ NOT \_ SUPPORTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




