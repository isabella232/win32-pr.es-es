---
description: La función BERGetInteger descodifica un entero con codificación BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Función BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911645"
---
# <a name="bergetinteger-function"></a>BERGetInteger función)

La función **BERGetInteger** descodifica un entero con codificación BER.

## <a name="syntax"></a>Sintaxis


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Puntero al entero que está descodificado.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Puntero al puntero al valor devuelto.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntero a la longitud de encabezado devuelta.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntero a la longitud de los datos.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntero al puntero a la entrada siguiente de BER.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si se encuentra y se convierte un entero codificado BER válido), el valor devuelto es **true**.

Si la función no es correcta, el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Analizador. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




