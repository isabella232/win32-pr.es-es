---
description: Describe cómo usar los métodos comunes de las interfaces de colección.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Trabajar con interfaces de colección DE OM xps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570533"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Trabajar con interfaces de colección DE OM xps

Describe cómo usar los métodos comunes de las interfaces de colección.

## <a name="contents"></a>Contenido

Los métodos descritos en esta sección se muestran en la lista siguiente. No todas las interfaces de colección admiten cada uno de estos métodos y algunas interfaces también admiten métodos que no se describen en esta página. Para obtener la lista de métodos admitidos por una interfaz específica, consulte la descripción de la descripción de esa interfaz.

<dl>

[Append (método)](#append-method)  
[GetAt (método)](#getat-method)  
[GetCount (Método)](#getcount-method)  
[InsertAt (método)](#insertat-method)  
[RemoveAt (método)](#removeat-method)  
[SetAt (método)](#setat-method)  
</dl>

[Consulte también](#see-also)

## <a name="append-method"></a>Append (método)

Anexa un objeto al final de la colección.

**Sintaxis genérica**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Descripción**

Al final de la colección, este método anexa un objeto que se pasa en la lista de parámetros, como se muestra en el diagrama siguiente.

![una ilustración que muestra cómo anexar agrega una entrada a la colección](images/generic-append.png)

## <a name="getat-method"></a>GetAt (método)

Obtiene un objeto de una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Descripción**

Escribe el objeto almacenado en la ubicación de la colección especificada por *index* en la variable a la que hace referencia el *objeto*. Esta acción no cambia el contenido de la colección. En el siguiente diagrama se muestra este proceso.

![una ilustración que muestra cómo getat recupera una entrada de la colección](images/generic-getat.png)

## <a name="getcount-method"></a>GetCount (Método)

Obtiene el número de objetos almacenados en la colección.

**Sintaxis genérica**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Descripción**

Escribe el número de objetos almacenados actualmente en la colección en la variable a la que hace referencia *count.* Esta acción no cambia el contenido de la colección. En el siguiente diagrama se muestra este proceso.

![una ilustración que muestra cómo getcount obtiene el número de entradas de la colección](images/generic-getcount.png)

## <a name="insertat-method"></a>InsertAt (método)

Inserta un objeto en una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descripción**

El objeto que se pasa *en el objeto* se inserta en la colección en la ubicación especificada por el *índice*. Antes de insertar el nuevo objeto *,* este método mueve en 1 el objeto que previamente ha ocupado la ubicación en *el* índice y mueve todos los punteros de interfaz posteriores al *índice*. En el siguiente diagrama se muestra este proceso.

![una ilustración que muestra cómo insertat agrega una entrada a la colección](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt (método)

Quita el objeto de una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Descripción**

Este método libera el objeto de la ubicación especificada por *index* y, a continuación, compacta la colección reduciendo en 1 el índice de cada puntero posterior al *índice*. En el siguiente diagrama se muestra este proceso.

![una ilustración que muestra cómo removeat quita una entrada de la colección](images/generic-removeat.png)

## <a name="setat-method"></a>SetAt (método)

Reemplaza el objeto en una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descripción**

Este método libera primero el objeto en la ubicación a la que hace referencia el índice *y,* a continuación, reemplaza ese objeto por el que se pasa en el *objeto*. En el siguiente diagrama se muestra este proceso.

![una ilustración que muestra cómo setat reemplaza una entrada de la colección](images/generic-setat.png)

## <a name="see-also"></a>Consulte también

<dl>

[**IXpsOMColorProfileResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**IXpsOMGradientStopCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**IXpsOMSignatureBlockResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



