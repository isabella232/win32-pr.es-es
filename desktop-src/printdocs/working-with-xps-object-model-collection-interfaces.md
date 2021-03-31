---
description: Describe cómo usar los métodos comunes de las interfaces de colección.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Trabajar con interfaces de colección de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277436"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Trabajar con interfaces de colección de XPS OM

Describe cómo usar los métodos comunes de las interfaces de colección.

## <a name="contents"></a>Contenido

Los métodos descritos en esta sección se muestran en la lista siguiente. No todas las interfaces de colección admiten cada uno de estos métodos, y algunas interfaces también admiten métodos que no se describen en esta página. Para obtener la lista de métodos admitidos por una interfaz específica, consulte la descripción de la descripción de la interfaz.

<dl>

[Append (método)](#append-method)  
[GetAt (método)](#getat-method)  
[Método GetCount](#getcount-method)  
[Método Insertat (](#insertat-method)  
[RemoveAt (método)](#removeat-method)  
[Método SetAt](#setat-method)  
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

Al final de la colección, este método anexa un objeto que se pasa en la lista de parámetros, tal y como se muestra en el diagrama siguiente.

![una figura que muestra cómo Append agrega una entrada a la colección](images/generic-append.png)

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

Escribe el objeto almacenado en la ubicación de la colección especificada por el *Índice* en la variable a la que hace referencia el *objeto*. Esta acción no cambia el contenido de la colección. En el siguiente diagrama se muestra este proceso.

![una figura que muestra cómo getadt recupera una entrada de la colección.](images/generic-getat.png)

## <a name="getcount-method"></a>Método GetCount

Obtiene el número de objetos almacenados en la colección.

**Sintaxis genérica**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Descripción**

Escribe el número de objetos que están almacenados actualmente en la colección en la variable a la que hace referencia el *recuento*. Esta acción no cambia el contenido de la colección. En el siguiente diagrama se muestra este proceso.

![una figura que muestra cómo getCount obtiene el número de entradas de la colección.](images/generic-getcount.png)

## <a name="insertat-method"></a>Método Insertat (

Inserta un objeto en la ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descripción**

El objeto que se pasa en el *objeto* se inserta en la colección en la ubicación especificada por *index*. Antes de insertar el nuevo *objeto*, este método se mueve por 1 el objeto que ha ocupado previamente la ubicación en el *Índice* y mueve todos los punteros de interfaz después al *Índice*. En el siguiente diagrama se muestra este proceso.

![una figura que muestra cómo insertat (agrega una entrada a la colección](images/generic-insertat.png)

## <a name="removeat-method"></a>RemoveAt (método)

Quita el objeto de una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Descripción**

Este método libera el objeto de la ubicación especificada por el *Índice* y, a continuación, compacta la colección reduciendo en 1 el índice de cada puntero después del *Índice*. En el siguiente diagrama se muestra este proceso.

![una figura que muestra cómo RemoveAt quita una entrada de la colección.](images/generic-removeat.png)

## <a name="setat-method"></a>Método SetAt

Reemplaza el objeto situado en una ubicación especificada de la colección.

**Sintaxis genérica**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descripción**

Este método libera primero el objeto en la ubicación a la que hace referencia el *Índice* y, a continuación, reemplaza ese objeto por el que se pasa en el *objeto*. En el siguiente diagrama se muestra este proceso.

![una figura que muestra cómo setat reemplaza una entrada en la colección](images/generic-setat.png)

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

 

 



