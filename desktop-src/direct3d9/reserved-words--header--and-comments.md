---
description: En la tabla siguiente se muestra qué palabras están reservadas y no se deben usar.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palabras reservadas, encabezado y comentarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f583084b3faa4777a5fe6031cc247fdb99c27cc1fb23c6a5676e60afe00aba20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044285"
---
# <a name="reserved-words-header-and-comments"></a>Palabras reservadas, encabezado y comentarios

En la tabla siguiente se muestra qué palabras están reservadas y no se deben usar.

| Palabras reservadas | Palabras reservadas | Palabras reservadas|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| RECURSO \_ BINARIO | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| Cstring          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

El encabezado de longitud variable es obligatorio y debe estar al principio del flujo de datos. El encabezado contiene los datos siguientes.



| Tipo           | Requerido | Tamaño (en bytes) | Value | Descripción                  |
|----------------|----------|-----------------|-------|------------------------------|
| Número mágico   | x        | 4               | Xof   |                              |
| Número de versión | x        | 2               | 03    | Versión principal 3              |
|                |          |                 | 03    | Versión secundaria 3              |
| Tipo de formato    | x        | 4               | txt   | Archivo de texto                    |
|                |          |                 | bin   | Archivo binario                  |
|                |          |                 | tzip  | Archivo de texto comprimido de MSZip   |
|                |          |                 | bzip  | Archivo binario comprimido de MSZip |
| Tamaño float     | x        | 0064            |       | Flotantes de 64 bits                |
|                | x        | "0032"          |       | Flotantes de 32 bits                |



 

Los valores de la tabla se delimitan entre comillas para llamar la atención sobre el número de caracteres de cada valor. Aquellos con 4 bytes contienen cuatro caracteres, los que tienen 2 bytes contienen dos caracteres.

Los comentarios solo son aplicables en archivos de texto. Los comentarios pueden producirse en cualquier parte del flujo de datos. Un comentario comienza con barras diagonales dobles de estilo C++ (//) o un signo de perd ( \# ). El comentario se ejecuta hasta la siguiente línea nueva. En el ejemplo siguiente se muestran comentarios válidos.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de texto](text-encoding.md)
</dt> </dl>

 

 



