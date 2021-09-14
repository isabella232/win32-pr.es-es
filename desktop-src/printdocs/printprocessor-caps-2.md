---
description: Representa la información de funcionalidad de la impresora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: PRINTPROCESSOR_CAPS_2 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359704"
---
# <a name="printprocessor_caps_2-structure"></a>PRINTPROCESSOR \_ CAPS \_ 2 (estructura)

Representa la información de funcionalidad de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a>Members

<dl> <dt>

**dwLevel**
</dt> <dd>

Valor que indica el número de versión de la estructura.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Máscara de bits que representa los distintos números de páginas de documento que la impresora puede imprimir en un solo lado de una hoja física. El bit menos significativo representa una página de documento por lado, el bit siguiente representa 2 páginas de documento por lado, y así sucesivamente. Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por lado físico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Valor de marca que indica el orden en el que se imprimirán las páginas. Puede ser **NORMAL \_ PRINT,** **REVERSE \_ PRINT** o **LA IMPRESIÓN \_ INVERTIDA.**

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Número máximo de copias que la impresora puede controlar.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Patrones disponibles cuando se imprimen varias páginas de documento en el mismo lado de una hoja de papel. Las marcas posibles son las siguientes:



| Value                     | Significado                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ RIGHT \_ THEN \_ DOWN | Las páginas aparecen en filas de derecha a izquierda, cada fila posterior por debajo de su predecesor.                 |
| PPCAPS \_ DOWN \_ THEN \_ RIGHT | Las páginas aparecen en columnas de arriba abajo, cada columna posterior a la derecha de su predecesor. |
| PPCAPS \_ LEFT \_ THEN \_ DOWN  | Las páginas aparecen en filas de izquierda a derecha, cada fila posterior por debajo de su predecesor.                 |
| PPCAPS \_ ABAJO Y A LA \_ \_ IZQUIERDA  | Las páginas aparecen en columnas de arriba abajo, cada columna posterior a la izquierda de su predecesor.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Solo puede ser PPCAPS BORDER PRINT, lo que indica que, cuando se imprimen varias páginas de documento en un solo lado de una hoja física, se puede indicar a la impresora si se debe imprimir o no un borde alrededor del área de imagen de cada página de \_ \_ documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Solo puede ser PPCAPS \_ RESALTE \_ EDGE, lo que indica que la impresora puede imprimir el estilo de los folletos.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Value                                         | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PÁGINAS INVERSAS DE PPCAPS \_ \_ PARA \_ \_ DÚPLEX \_ INVERSO  | Al imprimir en orden inverso y dúplex, el procesador puede imprimir intercambiar el orden de cada par de páginas, por lo que en lugar de imprimir en orden 4,3,2,1, imprimirá en el orden 3,4,1,2.                                                                                                       |
| PPCAPS \_ NO ENVÍA PÁGINAS \_ \_ ADICIONALES PARA \_ \_ \_ DÚPLEX | Cuando se dúplex, se puede decir al procesador de impresión que no envíe una página adicional cuando hay un número impar de páginas de documento. El procesador respetará el valor lo mejor posible, pero en los casos en los que impedir una página en blanco adicional provocaría una salida incorrecta, se pueden enviar las páginas adicionales. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Solo puede ser PPCAPS \_ SQUARE \_ SCALING, lo que indica que la impresora puede escalar la imagen de página.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **GetPrintProcessorCapabilities** proporciona valores para todos los miembros de la estructura, que se documenta en Windows Driver Kit.

Cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), el colador llama a la función **GetPrintProcessorCapabilities** de un procesador de impresión y especifica un nombre de valor que tiene un formato de tipo de datos **PrintProcCaps \_**_,_ donde *datatype* es el nombre de un tipo de datos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




