---
description: La estructura SET define un conjunto de valores.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: ESTABLECER estructura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276835"
---
# <a name="set-structure"></a>ESTABLECER estructura

La estructura **set** define un conjunto de valores.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>Miembros

<dl> <dt>

**nEntries**
</dt> <dd>

Número total de entradas de un conjunto.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Puntero a una matriz de valores de BYTE.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Puntero a una matriz de valores de WORD.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Puntero a una matriz de valores DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Puntero a una matriz de estructuras [LARGEINT](largeint.md) .

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Puntero a una matriz de valores SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Puntero a una matriz de estructuras de [ \_ bytes etiquetadas](labeled-byte.md) . Cada estructura de **\_ bytes con etiqueta** define un valor y una etiqueta. Monitor de red muestra una etiqueta si encuentra un valor correspondiente en el paquete del protocolo.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Puntero a una matriz de estructuras de [ \_ palabras etiquetadas](labeled-word.md) que definen un conjunto de valores y etiquetas de palabra.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Puntero a una matriz de estructuras [ \_ DWORD con etiqueta](labeled-dword.md) que definen un conjunto de valores DWORD y etiquetas.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Puntero a una matriz de estructuras [ \_ LARGEINT con etiqueta](labeled-largeint.md) que definen un conjunto de valores y etiquetas LARGEINT.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Puntero a una matriz de estructuras [ \_ SYSTEMTIME etiquetadas](labeled-systemtime.md) que definen un conjunto de valores del sistema y etiquetas.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Puntero a una matriz de estructuras de [ \_ bits con etiqueta](labeled-bit.md) que definen un conjunto de pares de bits con etiqueta. Cada BIT puede especificar dos etiquetas para cada Estado (0 o 1) del BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Puntero a una matriz de valores.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **set** se usa para definir un conjunto de datos de comparación que monitor de red pueden utilizar para interpretar el valor de una propiedad en un paquete de protocolo. Cuando se requiere un conjunto de datos de comparación, se especifica un puntero a la estructura de **conjunto** en el miembro **lpSet** de la estructura [PROPERTYINFO](propertyinfo.md) .

El archivo DLL del analizador puede proporcionar un conjunto de valores y un conjunto de etiquetas. El miembro de la **Unión** que selecciona en una estructura de **conjunto** apunta a una matriz de estructuras que definen cada miembro de un conjunto.

-   Conjunto de valores

    Se utiliza un conjunto de valores cuando se desea que Monitor de red incluya un indicador in-set o Not-in-set con el valor que se encuentra en el paquete del protocolo. Por ejemplo, si se especifica un conjunto DWORD, Monitor de red muestra una etiqueta para cada valor DWORD que se encuentra en el paquete de protocolo, lo que indica que la DWORD es o no se especifica en el conjunto.

    Un conjunto de valores puede basarse en los tipos de datos BYTE, WORD, DWORD, LARGEINT y SYSTEMTIME.

-   Conjunto de etiquetas

    Se utiliza un conjunto de etiquetas cuando se desea Monitor de red mostrar una etiqueta definida por el usuario en lugar de los valores de propiedad especificados en un conjunto.

    Un conjunto de etiquetas puede basarse en pares de BYTEs, palabras, DWORD, LARGEINT, SYSTEMTIME y de etiquetas de bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[BIT con etiqueta \_](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




