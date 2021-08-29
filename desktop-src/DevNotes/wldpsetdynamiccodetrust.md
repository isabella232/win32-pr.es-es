---
description: Establece un código dinámico de .NET CRL en disco confiable para .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Función WldpSetDynamicCodeTrust (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 5a7277f13596ff3d397c97c8e8260e57e0e444e6943ba68f073f90c90cf3583d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075648"
---
# <a name="wldpsetdynamiccodetrust-function"></a>Función WldpSetDynamicCodeTrust

Establece un código dinámico de .NET CRL en disco confiable para .NET.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileHandle* 
</dt> <dd>

Identificador de un archivo de código dinámico en disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ OK si se** realiza correctamente o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




