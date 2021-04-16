---
description: Especifica si un estilo que no es de color tiene el estilo de negrita.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650055"
---
# <a name="fboldimestyle-function"></a>FBoldIMEStyle función)

Especifica si un estilo que no es de color tiene el estilo de negrita.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pimestyle* \[ de\]
</dt> <dd>

Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si el estilo tiene el estilo de negrita.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
