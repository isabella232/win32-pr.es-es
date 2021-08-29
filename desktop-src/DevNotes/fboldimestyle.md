---
description: Especifica si un estilo que no es de color tiene el estilo en negrita.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: Función FBoldIMEStyle
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
ms.openlocfilehash: a6d25483edb9aa09febccc0b375ee34152641aa75a4101b5ee34900e4df29031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758645"
---
# <a name="fboldimestyle-function"></a>Función FBoldIMEStyle

Especifica si un estilo que no es de color tiene el estilo en negrita.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pimestyle* \[ En\]
</dt> <dd>

Estructura **IMESTYLE** devuelta desde la [**función PIMEStyleFromAttr.**](pimestylefromattr.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE** si el estilo tiene el estilo en negrita.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
