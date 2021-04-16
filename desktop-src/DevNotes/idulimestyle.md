---
description: Identifica si el estilo que no es de color especificado tiene subrayado.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650001"
---
# <a name="idulimestyle-function"></a>IdUlIMEStyle función)

Identifica si el estilo que no es de color especificado tiene subrayado.

## <a name="syntax"></a>Sintaxis


```C++
UINT __cdecl IdUlIMEStyle(
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

Esta función puede devolver uno de los valores siguientes.

<dl> <dt>

**IMESTY \_ UL \_ min** (2002)
</dt> <dt>

**IMESTY \_ UL \_ ninguno** (2002)
</dt> <dt>

**IMESTY \_ UL \_ único** (2003)
</dt> <dt>

**IMESTY \_ UL \_ puntos** (2005)
</dt> <dt>

**IMESTY \_ \_Gruesa UL** (2006)
</dt> <dt>

**IMESTY \_ UL \_ inferior** (2011)
</dt> <dt>

**IMESTY \_ UL \_ THICKLOWER** (2012)
</dt> <dt>

**IMESTY \_ UL \_ THICKDITHLOWER** (2013)
</dt> <dt>

**IMESTY \_ UL \_ DITHLOWER** (2014)
</dt> <dt>

**IMESTY \_ UL \_ máx** . (2014)
</dt> </dl>

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

 

 
