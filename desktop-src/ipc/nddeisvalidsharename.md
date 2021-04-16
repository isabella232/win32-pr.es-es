---
description: Determina si un nombre de recurso compartido utiliza la sintaxis correcta.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Función NDdeIsValidShareName (Nddeapi. h)
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
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686528"
---
# <a name="nddeisvalidsharename-function"></a>NDdeIsValidShareName función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Determina si un nombre de recurso compartido utiliza la sintaxis correcta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombreDeRecursoCompartido* \[ de\]
</dt> <dd>

Nombre del recurso compartido que se va a validar. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el nombre del recurso compartido tiene una sintaxis válida, el valor devuelto es distinto de cero.

Si el nombre del recurso compartido no tiene una sintaxis válida, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeIsValidShareNameW** (Unicode) y **NDdeIsValidShareNameA** (ANSI)<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




