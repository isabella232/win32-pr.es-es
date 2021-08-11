---
description: El tipo de posición de una tabla de contenido
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: El tipo de posición de una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f94f23e185b46f52123a80a0d27f7fefffcaff7e711a5e9718e07dab7da40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237899"
---
# <a name="the-position-type-of-a-table-of-contents"></a>El tipo de posición de una tabla de contenido

Algunos métodos de [**la interfaz ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) tienen un parámetro denominado *enumTocPosType* que tiene un tipo [**de enumeración TOC \_ POS \_ TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Este parámetro especifica la posición en un archivo multimedia donde se almacena una tabla de contenido. La intención era que la tabla de contenido se pudiera almacenar en el encabezado de archivo o en el cuerpo del archivo como un objeto de nivel superior. Esta funcionalidad aún no se ha implementado.

Actualmente, las tablas de contenido solo se pueden almacenar como objetos de nivel superior, por lo que siempre debe establecer el parámetro *enumTocPosType* en **TOC \_ POS \_ TOPLEVELOBJECT**. Si establece *enumTocPosType* en **TOC \_ POS \_ INHEADER**, el método devolverá **E \_ NOTIMPL**.

Los métodos siguientes tienen un *parámetro enumTocPosType.*

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

 

 



