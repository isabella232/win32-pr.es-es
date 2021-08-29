---
description: La función IsRemoteNPP indica si el BLOB especificado especifica un NPP remoto.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Función IsRemoteNPP (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: ec91b5e2d4602df6aa264a27adf46e47cec24683fc65dace358649eeba76643a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890335"
---
# <a name="isremotenpp-function"></a>Función IsRemoteNPP

La **función IsRemoteNPP** indica si el BLOB especificado especifica un NPP remoto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador de un BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **TRUE.**

## <a name="remarks"></a>Comentarios

Use esta función para probar si existe una categoría remota.

Asegúrese de que los nombres de equipo remoto y local son diferentes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




