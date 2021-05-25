---
description: En la tabla siguiente se muestra qué palabras están reservadas y no se deben usar.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palabras reservadas, encabezado y comentarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343660"
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



| Tipo           | Requerido | Tamaño (en bytes) | Valor | Descripción                  |
|----------------|----------|-----------------|-------|------------------------------|
| Número mágico   | x        | 4               | Xof   |                              |
| Número de versión | x        | 2               | 03    | Versión principal 3              |
|                |          |                 | 03    | Versión secundaria 3              |
| Tipo de formato    | x        | 4               | txt   | Archivo de texto                    |
|                |          |                 | bin   | Archivo binario                  |
|                |          |                 | tzip  | Archivo de texto comprimido MSZip   |
|                |          |                 | bzip  | Archivo binario comprimido de MSZip |
| Tamaño flotante     | x        | 0064            |       | Flotantes de 64 bits                |
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

 

 



