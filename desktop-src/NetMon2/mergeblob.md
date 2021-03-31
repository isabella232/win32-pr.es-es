---
description: La función MergeBlob copia todas las entradas del BLOB de origen en un BLOB de destino.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Función MergeBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001234"
---
# <a name="mergeblob-function"></a>MergeBlob función)

La función **MergeBlob** copia todas las entradas del BLOB de origen en un BLOB de destino.

## <a name="syntax"></a>Sintaxis


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDstBlob* \[ in, out\]
</dt> <dd>

Identificador del BLOB de destino. En la entrada, este BLOB contiene su información original. En la salida, este BLOB contiene su información original y toda la información del BLOB de origen.

</dd> <dt>

*hSrcBlob* \[ de\]
</dt> <dd>

Identificador del BLOB de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.

## <a name="remarks"></a>Observaciones

Las entradas comunes a los archivos de origen y de destino se sobrescribirán con los datos del BLOB de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




