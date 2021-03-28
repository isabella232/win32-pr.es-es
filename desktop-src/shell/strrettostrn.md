---
description: 'Toma una estructura STRRET devuelta por IShellFolder:: GetDisplayNameOf, la convierte en una cadena y coloca el resultado en un búfer.'
title: StrRetToStrN función)
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
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997953"
---
# <a name="strrettostrn-function"></a>StrRetToStrN función)

Toma una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) devuelta por [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), la convierte en una cadena y coloca el resultado en un búfer.

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

*pszOut* \[ enuncia\]
</dt> <dd>

Tipo: **LPTSTR**

Búfer que va a contener el nombre para mostrar. Se devolverá como una cadena terminada en NULL. Si *cchOut* es demasiado pequeño, el nombre se truncará para ajustarse.

</dd> <dt>

*cchOut* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño de *pszOut*, en caracteres. Si *cchOut* es demasiado pequeño, la cadena se truncará para ajustarse.

</dd> <dt>

*pStrRet* \[ in, out\]
</dt> <dd>

Tipo: **LPSTRRET**

Puntero a una estructura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Cuando la función devuelve, este puntero ya no será válido.

</dd> <dt>

*PIDL* \[ de\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntero a la estructura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

**True si es** correcto, **false** en caso de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> A partir de Shell32.dll versión 5,0, llamar a esta función es equivalente a llamar a [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**StrRetToStrN** no se exporta por nombre. Para usarlo, debe utilizar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 96 de Shell32.dll para obtener un puntero de función.

Si el miembro **uType** de la estructura a la que apunta *pStrRet* se establece en **Strret \_ WSTR**, el miembro **pOleStr** de esa estructura se liberará en la devolución.

Tenga en cuenta que esta función se exporta desde Shell32.dll en lugar de Shlwapi.dll. También se incluye en ShlObj. h en lugar de en shlwapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
