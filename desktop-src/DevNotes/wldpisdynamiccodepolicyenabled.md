---
description: Recupera un valor que describe el estado de cumplimiento de directivas de Device Guard para el código dinámico de .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Función WldpIsDynamicCodePolicyEnabled (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 12643bd542acac908c560a2094fb02e69d6d1aae62308e4ca4ece3be8bb85c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666366"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>Función WldpIsDynamicCodePolicyEnabled

Recupera un valor que describe el estado de cumplimiento de directivas de Device Guard para el código dinámico de .NET.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*isEnabled* \[ out\]
</dt> <dd>

Si se ejecuta **correctamente, devuelve true** si la directiva de Device Guard aplica la directiva de código dinámico de .NET; de lo contrario, devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ OK si se** realiza correctamente o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

El código dinámico hace referencia a código generado dinámicamente por CRL de .NET.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




