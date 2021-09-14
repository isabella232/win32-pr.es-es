---
title: Str_GetPtr función
description: Copia una cadena de un búfer a otro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr función Windows controles
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166974"
---
# <a name="str_getptr-function"></a>Función \_ Str GetPtr

\[Esta función está disponible a través Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Copia una cadena de un búfer a otro.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszSource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a una cadena de origen.

</dd> <dt>

*pszDest* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero al búfer de destino. Este valor puede ser **NULL.**

</dd> <dt>

*cchDest* \[ En\]
</dt> <dd>

Tipo: **int**

Tamaño de *pszDest,* en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si *pszDest* es **NULL** o *cchDest* es cero, devuelve el tamaño del búfer, en caracteres, necesario para contener una copia terminada en NULL de la cadena a la que apunta *pszSource*.

Si *pszDest* no es **NULL,** devuelve el número de caracteres copiados correctamente, incluido el carácter nulo final.

Si *pszDest* no puede contener toda la cadena a la que apunta *pszSource*, se copian los caracteres *(cchDest*-1), se devuelve la cadena terminada en NULL y *cchDest.*

## <a name="remarks"></a>Observaciones

**Str \_ GetPtr** está disponible como versiones ANSI (**Str \_ GetPtrA**) y Unicode (**Str \_ GetPtrW**). Estas funciones no se exportan por nombre ni se declaran en un archivo de encabezado público. Para usarlos, debe usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y solicitar ordinal 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) desde ComCtl32.dll para obtener un puntero de función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **Str \_ GetPtrW** (Unicode) y **Str \_ GetPtrA** (ANSI)<br/>                       |



 

