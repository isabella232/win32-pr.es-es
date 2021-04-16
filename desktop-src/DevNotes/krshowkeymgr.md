---
description: Muestra el cuadro de diálogo Administrador de claves en la interfaz de usuario.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr función)
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
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670419"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr función)

\[Esta función solo se incluye en Windows XP. No se incluye actualmente en ninguna otra versión de Windows ni se espera que se incluya en las versiones futuras de Windows.\]

Muestra el cuadro de diálogo Administrador de claves en la interfaz de usuario.

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

Este parámetro no se utiliza y debe establecerse en **null**.

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

Este parámetro no se utiliza y debe establecerse en **null**.

</dd> <dt>

*CmdShow* 
</dt> <dd>

Este parámetro no se utiliza y debe establecerse en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
