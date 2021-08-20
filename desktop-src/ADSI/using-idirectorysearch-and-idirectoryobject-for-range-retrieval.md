---
title: Uso de IDirectorySearch e IDirectoryObject para la recuperación de intervalos
description: Las interfaces IDirectoryObject o IDirectorySearch se pueden usar para recuperar un intervalo de valores de propiedad. Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI , uso de para la recuperación de miembros de un grupo
- IDirectoryObject ADSI , uso de para la recuperación de miembros de un grupo
- ADSI de recuperación de intervalos, mediante IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d061dd49c98bdb3b8cc731a28d0dc0ee5fe9a0df5816abf259ece17e456ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023063"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Uso de IDirectorySearch e IDirectoryObject para la recuperación de intervalos

Las [**interfaces IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) [**o IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se pueden usar para recuperar un intervalo de valores de propiedad. Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.

## <a name="range-retrieval-with-idirectoryobject"></a>Recuperación de intervalos con IDirectoryObject

La [**interfaz IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) se puede usar para la recuperación de intervalos especificando el atributo y el intervalo de uno de los atributos de la matriz *pAttributesName* al llamar al método [**IDirectoryObject::GetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para la recuperación de intervalos, vea Example [Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recuperación de intervalos con IDirectorySearch

La [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se puede usar para la recuperación de intervalos especificando el atributo y el intervalo de uno de los atributos recuperados en la matriz *pAttributesName* al llamar al método [**IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Cuando se usa la [**interfaz IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, hay un problema que se debe solucionar específicamente. Cuando el intervalo solicitado supera el número de valores restantes, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) devolverá **E ADS COLUMN NOT \_ \_ \_ \_ SET**. Para recuperar los valores restantes, es necesario usar el carácter comodín de intervalo ' \* '. Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos. Si se solicita entonces el intervalo 101-200, **IDirectorySearch::GetColumn** devolverá **E ADS COLUMN NOT \_ \_ \_ \_ SET**. Este problema se puede evitar mediante el método [**IDirectorySearch::GetNextColumnName.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) Normalmente, **GetNextColumnName devolverá** la cadena de consulta original. Sin embargo, cuando el intervalo solicitado supera el número de valores restantes, **GetNextColumnName** devolverá una versión modificada de la cadena de consulta reemplazando el valor de intervalo alto por el carácter comodín de intervalo ' \* '. En el ejemplo anterior, la primera consulta se realizaría con una cadena de atributo de "member;range=0-100" y **GetNextColumnName** devolverá "member;range=0-100". En la segunda consulta, la cadena de atributo sería "member;range=101-200", pero **GetNextColumnName** devolverá "member;range=101- \* ". Este caso se puede determinar comparando la cadena de atributo original con el resultado de **GetNextColumnName**. Si las cadenas son diferentes, el último bloque de valores debe solicitarse de nuevo con el carácter comodín de intervalo.

Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, vea Example [Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




