---
title: Str_GetPtr función)
description: Copia una cadena de un búfer a otro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr controles de función de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801532"
---
# <a name="str_getptr-function"></a>Str \_ GetPtr función)

\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

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

*pszSource* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero a una cadena de origen.

</dd> <dt>

*pszDest* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntero al búfer de destino. Este valor puede ser **null**.

</dd> <dt>

*cchDest* \[ de\]
</dt> <dd>

Tipo: **int**

Tamaño de *pszDest*, en caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **int**

Si *pszDest* es **null** o *cchDest* es cero, devuelve el tamaño del búfer, en caracteres, necesario para contener una copia terminada en NULL de la cadena a la que apunta *pszSource*.

Si *pszDest* no es **null**, devuelve el número de caracteres copiados correctamente, incluido el carácter nulo de terminación.

Si *pszDest* no puede contener la cadena completa a la que apunta *pszSource*, se copian los caracteres (*cchDest*-1), la cadena termina en NULL y se devuelve *cchDest* .

## <a name="remarks"></a>Observaciones

**Str \_ GetPtr** está disponible como versiones ANSI (**Str \_ GetPtrA**) y Unicode (**Str \_ GetPtrW**). Estas funciones no se exportan por nombre o se declaran en un archivo de encabezado público. Para usarlos, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) de ComCtl32.dll para obtener un puntero de función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **Str \_ GetPtrW** (Unicode) y **Str \_ GetPtrA** (ANSI)<br/>                       |



 

