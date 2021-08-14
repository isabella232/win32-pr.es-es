---
title: Procesamiento de los resultados de la búsqueda
description: Después de la primera llamada a IDirectorySearch GetFirstRow o IDirectorySearch GetNextRow, se devuelve \_ S OK, S ADS NOMORE ROWS o \_ un resultado de \_ \_ error.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Procesamiento de resultados de búsqueda ad
- Active Directory, Buscar, Procesar resultados de la búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185209"
---
# <a name="processing-the-search-results"></a>Procesamiento de los resultados de la búsqueda

Después de la primera llamada a [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), S **\_ OK**, **S ADS \_ \_ NOMORE \_ ROWS** o se devuelve un resultado de error.

Si el valor devuelto es **S \_ ADS \_ NOMORE \_ ROWS,** no se encontraron más objetos que coincidan con el filtro. Si se devuelve un resultado de error, se produce un error en la consulta. En ambos casos, no es necesario procesar las filas del resultado porque no se devolvió nada.

Si **se devuelve S \_ OK,** se ha recuperado una fila. Puede analizar las columnas por nombre mediante [**IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). El nombre es **el lDAPDisplayName** del atributo de la columna. El conjunto de todas las columnas se definió mediante el parámetro pAttributeNames del [**método IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) Si se especificó **NULL,** el conjunto de todas las columnas es la unión de todas las propiedades encontradas para todos los objetos devueltos. Para leer todo el conjunto de columnas devueltas para un objeto , use [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) para iterar cada columna y use el nombre de columna devuelto para llamar a **IDirectorySearch::GetColumn**.

El [**método IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) devuelve una estructura ADS SEARCH [**\_ \_ COLUMN**](/windows/desktop/api/iads/ns-iads-ads_search_column) que contiene el nombre del atributo, el tipo del atributo, el recuento de valores y un puntero a una matriz de estructuras [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que contienen los valores. Puede recorrer en bucle las estructuras **ADSVALUE** para leer los valores de la propiedad devuelta por la columna. Debe leer el miembro adecuado de la estructura **ADSVALUE** según el [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) especificado por el **miembro dwADsType** de la estructura **ADS SEARCH \_ \_ COLUMN** (o el miembro **dwType** de la estructura **ADSVALUE).** Por ejemplo, si **dwADsType** era **ADSTYPE \_ INTEGER**, leería el miembro **Integer** de cada **estructura ADSVALUE.**

Para obtener más información y un ejemplo de código, vea [Ejemplo de código para buscar usuarios.](example-code-for-searching-for-users.md)

 

 