---
description: Toma una estructura STRRET devuelta por IShellFolder::GetDisplayNameOf, la convierte en una cadena y coloca el resultado en un búfer.
title: Función StrRetToStrN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 26aadacec02ddca13da6a005ed70b27d1f0869ab8dbd159c553fc66fe19561bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675845"
---
# <a name="strrettostrn-function"></a>Función StrRetToStrN

Toma una [**estructura STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) devuelta por [**IShellFolder::GetDisplayNameOf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)la convierte en una cadena y coloca el resultado en un búfer.

## <a name="syntax"></a>Sintaxis


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszOut* \[ out\]
</dt> <dd>

Tipo: **LPTSTR**

Búfer para contener el nombre para mostrar. Se devolverá como una cadena terminada en NULL. Si *cchOut* es demasiado pequeño, el nombre se truncará para ajustarse.

</dd> <dt>

*cchOut* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño de *pszOut*, en caracteres. Si *cchOut* es demasiado pequeño, la cadena se truncará para ajustarse.

</dd> <dt>

*pStrRet* \[ in, out\]
</dt> <dd>

Tipo: **LPSTRRET**

Puntero a una [**estructura STRRET.**](/windows/desktop/api/Shtypes/ns-shtypes-strret) Cuando la función vuelva, este puntero ya no será válido.

</dd> <dt>

*pidl* \[ En\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntero a la estructura [**ITEMIDLIST del**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

**TRUE** si se ha hecho **correctamente, FALSE** en caso de error.

## <a name="remarks"></a>Comentarios

> [!Note]  
> A partir Shell32.dll versión 5.0, llamar a esta función equivale a llamar a [**StrRetToBuf.**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)

 

**StrRetToStrN** no se exporta por nombre. Para usarlo, debe usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 96 a Shell32.dll para obtener un puntero de función.

Si el **miembro uType** de la estructura a la que apunta *pStrRet* se establece en **STRRET \_ WSTR**, el **miembro pOleStr** de esa estructura se liberará al devolverse.

Tenga en cuenta que esta función se exporta desde Shell32.dll en lugar de Shlwapi.dll. También se incluye en Shlobj.h en lugar de en Shlwapi.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
