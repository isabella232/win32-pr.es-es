---
description: La función GetFrameRecognizeData devuelve una tabla de estructuras RECOGNIZEDATA. Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Función GetFrameRecognizeData (Netmon. h)
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
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000929"
---
# <a name="getframerecognizedata-function"></a>GetFrameRecognizeData función)

La función **GetFrameRecognizeData** devuelve una tabla de estructuras **RECOGNIZEDATA** . Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.

## <a name="syntax"></a>Sintaxis


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador de un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura **RECOGNIZEDATATABLE** .

Si la función no es correcta, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameRecognizeData** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




