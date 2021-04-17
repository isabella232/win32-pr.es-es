---
description: Representa la información de funcionalidad de la impresora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Estructura de PRINTPROCESSOR_CAPS_2 (winspool. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697497"
---
# <a name="printprocessor_caps_2-structure"></a>Estructura de PRINTPROCESSOR \_ Cap \_ 2

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



## <a name="members"></a>Miembros

<dl> <dt>

**dwLevel**
</dt> <dd>

Valor que indica el número de versión de la estructura.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Máscara de bits que representa los diversos números de páginas del documento que la impresora puede imprimir en un lado único de una hoja física. El bit menos significativo representa una página de documento por lado, el siguiente bit representa 2 páginas de documento por lado, etc. Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por lado físico.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Un valor de marca que indica el orden en el que se imprimirán las páginas. Puede ser impresión **normal \_**, impresión **inversa \_** o **folleto \_ impreso**.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Número máximo de copias que la impresora puede controlar.

</dd> <dt>

**dwNupDirectionCaps**
</dt> <dd>

Los patrones disponibles cuando se imprimen varias páginas del documento en el mismo lado de una hoja de papel. Las posibles marcas son las siguientes:



| Value                     | Significado                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| PPCAPS \_ a la derecha \_ \_ | Las páginas aparecen en filas de derecha a izquierda, cada fila subsiguiente debajo de su predecesor.                 |
| PPCAPS \_ \_ a la \_ derecha | Las páginas aparecen en columnas de arriba abajo, cada columna subsiguiente a la derecha de su predecesora. |
| PPCAPS \_ a la izquierda \_ \_  | Las páginas aparecen en filas de izquierda a derecha, cada fila subsiguiente debajo de su predecesor.                 |
| PPCAPS \_ \_ a la \_ izquierda  | Las páginas aparecen en columnas de arriba abajo, cada columna subsiguiente a la izquierda de su predecesora.  |



 

</dd> <dt>

**dwNupBorderCaps**
</dt> <dd>

Solo puede ser PPCAPS \_ Border \_ Print, lo que indica que, cuando se imprimen varias páginas del documento en una sola cara de una hoja física, se puede indicar a la impresora si se imprime o no un borde alrededor del área de impresión de cada página del documento.

</dd> <dt>

**dwBookletHandlingCaps**
</dt> <dd>

Solo puede ser PPCAPS \_ \_ , lo que indica que la impresora puede imprimir el estilo de folleto.

</dd> <dt>**dwDuplexHandlingCaps**</dt> <dd> 

| Value                                         | Significado                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPCAPS \_ páginas inversas \_ \_ para \_ dúplex inverso \_  | Al imprimir en orden inverso y dúplex, el procesador puede imprimir el orden de cada par de páginas, por lo que en lugar de imprimir en el orden 4, 3, 2, 1, se imprimirán en el orden 3, 4, 1, 2.                                                                                                       |
| PPCAPS \_ no \_ enviar \_ \_ páginas adicionales \_ para \_ dúplex | Al usar el dúplex, se puede indicar al procesador de impresión que no envíe una página adicional cuando hay un número impar de páginas del documento. El procesador respetará el valor de la mejor forma posible, pero en los casos en los que evitar una página en blanco adicional causaría una salida incorrecta, es posible que se sigan enviando las páginas adicionales. |



 

</dd> <dt>

**dwScalingCaps**
</dt> <dd>

Solo se puede \_ \_ escalar PPCAPS cuadrado, lo que indica que la impresora puede escalar la imagen de la página.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de todos los miembros de la estructura se proporcionan mediante la función **GetPrintProcessorCapabilities** , que se documenta en el kit de controladores de Windows.

Cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), el administrador de trabajos de impresión llama a la función **GetPrintProcessorCapabilities** de un procesador de impresión y especifica un nombre de valor que tiene un formato de **\_ PrintProcCaps**_DataType_, donde *DataType* es el nombre de un tipo de datos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

 




