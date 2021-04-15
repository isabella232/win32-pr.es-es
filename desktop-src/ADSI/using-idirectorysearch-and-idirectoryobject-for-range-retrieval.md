---
title: Usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos
description: Las interfaces IDirectoryObject o IDirectorySearch se pueden usar para recuperar un intervalo de valores de propiedad. Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, uso de para recuperar miembros de un grupo
- IDirectoryObject ADSI, uso de para recuperar miembros de un grupo
- ADSI de recuperación de intervalos con IDirectorySearch y IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656137"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Usar IDirectorySearch y IDirectoryObject para la recuperación de intervalos

Las interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) o [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se pueden usar para recuperar un intervalo de valores de propiedad. Para ello, especifique el atributo y el intervalo de uno de los atributos solicitados en la consulta.

## <a name="range-retrieval-with-idirectoryobject"></a>Recuperación de intervalos con IDirectoryObject

La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) se puede utilizar para la recuperación de intervalos especificando el atributo y el intervalo de uno de los atributos de la matriz *pAttributesName* al llamar al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para la recuperación de intervalos, vea el [código de ejemplo para el intervalo con IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recuperación de intervalos con IDirectorySearch

La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se puede usar para la recuperación por rangos especificando el atributo y el intervalo de uno de los atributos recuperados en la matriz *pAttributesName* al llamar al método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Cuando se usa la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, hay un problema que se debe solucionar de forma específica. Cuando el intervalo solicitado supera el número de valores restantes, [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) devolverá la **\_ columna E ADS \_ \_ no \_ establecida**. Para recuperar los valores restantes, es necesario usar el carácter comodín de intervalo ' \* '. Por ejemplo, si un grupo contiene 150 miembros, los valores de miembro 0-100 se pueden recuperar normalmente mediante la recuperación por intervalos. Si después se solicita el intervalo 101-200, **IDirectorySearch:: getcolumn (** devolverá la **\_ columna E ADS \_ \_ no \_ establecida**. Este problema se puede evitar mediante el método [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) . Normalmente, **GetNextColumnName** devolverá la cadena de consulta original. Sin embargo, cuando el intervalo solicitado supera el número de valores restantes, **GetNextColumnName** devolverá una versión modificada de la cadena de consulta reemplazando el valor de intervalo superior por el comodín de intervalo ' \* '. En el ejemplo anterior, la primera consulta se realizaría con una cadena de atributo de "Member; Range = 0-100" y **GetNextColumnName** devolverá "Member; Range = 0-100". En la segunda consulta, la cadena de atributo sería "Member; Range = 101-200", pero **GetNextColumnName** devolverá "Member; Range = 101- \* ". Este caso se puede determinar comparando la cadena de atributo original con el resultado de **GetNextColumnName**. Si las cadenas son diferentes, se debe volver a solicitar el último bloque de valores con el carácter comodín de intervalo.

Para obtener más información y un ejemplo de código que muestra cómo usar la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para la recuperación de intervalos, vea el [código de ejemplo para abarcar con IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




