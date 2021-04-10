---
description: Recupera un valor que describe el estado de aplicación de la Directiva de Device Guard para código dinámico de .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Función WldpIsDynamicCodePolicyEnabled (WLDP. h)
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
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152780"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>WldpIsDynamicCodePolicyEnabled función)

Recupera un valor que describe el estado de aplicación de la Directiva de Device Guard para código dinámico de .NET.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsEnabled* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve **true** si la Directiva de Device Guard aplica la Directiva de código dinámico .net; de lo contrario, devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

El código dinámico hace referencia al código generado dinámicamente de la CRL de .NET.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




