---
description: Descodifica y almacena una cadena.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Función CchLszOfId2
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
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815475"
---
# <a name="cchlszofid2-function"></a>Función CchLszOfId2

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

*identificador* 
</dt> <dd>

Identificador de la cadena del archivo de recursos que se va a descodificar y almacenar. No se comprueba la validez de la cadena.

</dd> <dt>

*Lsz* 
</dt> <dd>

Puntero a un búfer con una longitud de *cbmax*. Las cadenas que son más largas *que cbmax* se truncan.

</dd> <dt>

*cbmax* 
</dt> <dd>

Longitud máxima de la cadena que se va a almacenar en el *parámetro lsz.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve la cadena descodificada.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
