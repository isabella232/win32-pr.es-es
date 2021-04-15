---
description: En la tabla siguiente se muestran las palabras que están reservadas y no se deben usar.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palabras reservadas, encabezado y comentarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536819"
---
# <a name="reserved-words-header-and-comments"></a>Palabras reservadas, encabezado y comentarios

En la tabla siguiente se muestran las palabras que están reservadas y no se deben usar.



|                  |          |           |
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| recurso BINARIo \_ | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

El encabezado de longitud variable es obligatorio y debe estar al principio del flujo de datos. El encabezado contiene los datos siguientes.



| Tipo           | Obligatorio | Tamaño (en bytes) | Value | Descripción                  |
|----------------|----------|-----------------|-------|------------------------------|
| Número mágico   | x        | 4               | xof   |                              |
| Número de versión | x        | 2               | 03    | Versión principal 3              |
|                |          |                 | 03    | Versión secundaria 3              |
| Tipo de formato    | x        | 4               | txt   | Archivo de texto                    |
|                |          |                 | bin   | Archivo binario                  |
|                |          |                 | tzip  | MSZip archivo de texto comprimido   |
|                |          |                 | bzip  | MSZip archivo binario comprimido |
| Tamaño de Float     | x        | 0064            |       | floats de 64 bits                |
|                | x        | "0032"          |       | floats de 32 bits                |



 

Los valores de la tabla están delimitados por comillas para llamar la atención al número de caracteres de cada valor. Aquellos con 4 bytes contienen cuatro caracteres, los cuales tienen 2 bytes y dos.

Los comentarios solo se aplican en archivos de texto. Los comentarios pueden aparecer en cualquier parte del flujo de datos. Un comentario comienza con barras diagonales dobles de estilo de C++ (//) o con un signo de almohadilla ( \# ). El comentario se ejecuta en la siguiente línea nueva. En el ejemplo siguiente se muestran comentarios válidos.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de texto](text-encoding.md)
</dt> </dl>

 

 



