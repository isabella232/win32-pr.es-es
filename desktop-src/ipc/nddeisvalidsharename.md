---
description: Determina si un nombre de recurso compartido usa la sintaxis adecuada.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Función NDdeIsValidShareName (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 3e289429047d8d1cee4f525a9f45a9abe1dd8eb51bcf57e83e39876fba9a5a89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964005"
---
# <a name="nddeisvalidsharename-function"></a>Función NDdeIsValidShareName

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Determina si un nombre de recurso compartido usa la sintaxis adecuada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*shareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido que se va a validar. Este parámetro no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el nombre del recurso compartido tiene una sintaxis válida, el valor devuelto es distinto de cero.

Si el nombre del recurso compartido no tiene una sintaxis válida, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido de DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeIsValidShareNameW** (Unicode) y **NDdeIsValidShareNameA** (ANSI)<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




