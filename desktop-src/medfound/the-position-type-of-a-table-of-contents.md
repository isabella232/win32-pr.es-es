---
description: El tipo de posición de una tabla de contenido
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: El tipo de posición de una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696882"
---
# <a name="the-position-type-of-a-table-of-contents"></a>El tipo de posición de una tabla de contenido

Algunos métodos de la interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) tienen un parámetro denominado *enumTocPosType* que tiene un tipo de [**tipo de \_ pos \_ de TDC de enumeración**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Este parámetro especifica la posición en un archivo multimedia donde se almacena una tabla de contenido. La intención era que la tabla de contenido podía almacenarse en el encabezado de archivo o en el cuerpo del archivo como un objeto de nivel superior. Esta funcionalidad no se ha implementado todavía.

Actualmente, las tablas de contenido solo se pueden almacenar como objetos de nivel superior, por lo que siempre debe establecer el parámetro *enumTocPosType* en el **TOPLEVELOBJECT de \_ pos \_ de TDC**. Si establece *enumTocPosType* en el **\_ \_ inencabezado de pos de TDC**, el método devolverá **E \_ NOTIMPL**.

Los métodos siguientes tienen un parámetro *enumTocPosType* .

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación del analizador de tabla de contenido](toc-parser-programming-guide.md)
</dt> </dl>

 

 



