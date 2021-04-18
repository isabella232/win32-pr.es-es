---
description: Descodifica y almacena una cadena.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661063"
---
# <a name="cchlszofid2-function"></a>CchLszOfId2 función)

Descodifica y almacena una cadena.

## <a name="syntax"></a>Sintaxis


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* 
</dt> <dd>

El identificador de la cadena en el archivo de recursos que se va a descodificar y almacenar. No se comprueba la validez de la cadena.

</dd> <dt>

*lsz* 
</dt> <dd>

Un puntero a un búfer con una longitud de *cbmax*. Las cadenas que son más largas que *cbmax* se truncan.

</dd> <dt>

*cbmax* 
</dt> <dd>

Longitud máxima de la cadena que se va a almacenar en el parámetro *LSZ* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve la cadena descodificada.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
