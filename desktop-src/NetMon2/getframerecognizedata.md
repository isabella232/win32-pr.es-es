---
description: La función GetFrameRecognizeData devuelve una tabla de estructuras RECOGNIZEDATA. Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Función GetFrameRecognizeData (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366503"
---
# <a name="getframerecognizedata-function"></a>Función GetFrameRecognizeData

La **función GetFrameRecognizeData** devuelve una tabla de estructuras **RECOGNIZEDATA.** Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.

## <a name="syntax"></a>Sintaxis


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador de un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un puntero a una **estructura RECOGNIZEDATATABLE.**

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetFrameRecognizeData.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




