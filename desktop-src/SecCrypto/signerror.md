---
description: Llama a la función GetLastError y convierte el código de retorno en HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082183"
---
# <a name="signerror-function"></a>SignError función)

> [!IMPORTANT]
> Esta API está en desuso. Microsoft puede quitar esta API en futuras versiones.

 

La función **SignError** llama a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y convierte el código de retorno en **HRESULT**.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve **S \_ correcto**.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
