---
description: Abre el cuadro de diálogo del administrador de claves en la interfaz de usuario.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: Función KRShowKeyMgr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 58b62b036b1aba7916c2c08cdbdb137e136c85c694dc11210cadcd7fe2a92d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004137"
---
# <a name="krshowkeymgr-function"></a>Función KRShowKeyMgr

\[Esta función solo se incluye en Windows XP. Actualmente no se incluye en ninguna otra versión de Windows, ni se espera que se incluya en versiones futuras de Windows.\]

Abre el cuadro de diálogo del administrador de claves en la interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwParent* 
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo. Este parámetro puede ser **NULL**.

</dd> <dt>

*hInstance* 
</dt> <dd>

Este parámetro no se usa y debe establecerse en **NULL.**

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

Este parámetro no se usa y debe establecerse en **NULL.**

</dd> <dt>

*CmdShow* 
</dt> <dd>

Este parámetro no se usa y debe establecerse en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
