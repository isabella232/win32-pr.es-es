---
description: La estructura SET define un conjunto de valores.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: Estructura SET (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260367"
---
# <a name="set-structure"></a>Set (estructura)

La **estructura SET** define un conjunto de valores.

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



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Número total de entradas de un conjunto.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Puntero a una matriz de valores BYTE.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Puntero a una matriz de valores WORD.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Puntero a una matriz de valores DWORD.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Puntero a una matriz de [estructuras LARGEINT.](largeint.md)

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Puntero a una matriz de valores SYSTEMTIME.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Puntero a una matriz de [estructuras \_ LABELED BYTE.](labeled-byte.md) Cada **estructura \_ LABELED BYTE** define un valor y una etiqueta. Monitor de red muestra una etiqueta si encuentra un valor correspondiente en el paquete de protocolo.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Puntero a una matriz de [estructuras LABELED \_ WORD](labeled-word.md) que definen un conjunto de valores y etiquetas de WORD.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Puntero a una matriz de [estructuras \_ DWORD LABELED](labeled-dword.md) que definen un conjunto de etiquetas y valores DWORD.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Puntero a una matriz de [estructuras \_ LABELED LARGEINT](labeled-largeint.md) que definen un conjunto de etiquetas y valores LARGEINT.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Puntero a una matriz [de estructuras \_ LABELED SYSTEMTIME](labeled-systemtime.md) que definen un conjunto de etiquetas y valores system.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Puntero a una matriz de [estructuras LABELED \_ BIT](labeled-bit.md) que definen un conjunto de pares BIT etiquetados. Cada BIT puede especificar dos etiquetas una etiqueta para cada estado (0 o 1) del BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Puntero a una matriz de valores.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **estructura SET** se usa para definir un conjunto de datos de comparación que Monitor de red usar para interpretar el valor de una propiedad en un paquete de protocolo. Cuando se requiere un conjunto de datos de comparación, se especifica un puntero a la **estructura SET** en el **miembro lpSet** de la [estructura PROPERTYINFO.](propertyinfo.md)

El archivo DLL del analizador puede proporcionar un conjunto de valores y un conjunto de etiquetas. El miembro de **UNION** que seleccione en una estructura **SET** apunta a una matriz de estructuras que definen cada miembro de un conjunto.

-   Conjunto de valores

    Un conjunto de valores se usa cuando Monitor de red incluir un indicador in-set o not-in-set con el valor que se encuentra en el paquete de protocolo. Por ejemplo, si se especifica un conjunto DWORD, Monitor de red muestra una etiqueta para cada valor DWORD que se encuentra en el paquete de protocolo, lo que indica que DWORD es o no se especifica en el conjunto.

    Un conjunto de valores puede basarse en los tipos de datos BYTE, WORD, DWORD, LARGEINT y SYSTEMTIME.

-   Conjunto de etiquetas

    Un conjunto de etiquetas se usa cuando Monitor de red mostrar una etiqueta definida por el usuario en lugar de los valores de propiedad especificados en un conjunto.

    Un conjunto de etiquetas puede basarse en los pares de etiquetas BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME y BIT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[BIT \_ ETIQUETADO](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




