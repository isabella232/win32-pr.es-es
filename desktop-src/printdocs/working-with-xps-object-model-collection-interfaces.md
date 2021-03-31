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
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="a4185-103">Trabajar con interfaces de colección de XPS OM</span><span class="sxs-lookup"><span data-stu-id="a4185-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="a4185-104">Describe cómo usar los métodos comunes de las interfaces de colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="a4185-105">Contenido</span><span class="sxs-lookup"><span data-stu-id="a4185-105">Contents</span></span>

<span data-ttu-id="a4185-106">Los métodos descritos en esta sección se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4185-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="a4185-107">No todas las interfaces de colección admiten cada uno de estos métodos, y algunas interfaces también admiten métodos que no se describen en esta página.</span><span class="sxs-lookup"><span data-stu-id="a4185-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="a4185-108">Para obtener la lista de métodos admitidos por una interfaz específica, consulte la descripción de la descripción de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a4185-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="a4185-109">Append (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="a4185-110">GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="a4185-111">Método GetCount</span><span class="sxs-lookup"><span data-stu-id="a4185-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="a4185-112">Método Insertat (</span><span class="sxs-lookup"><span data-stu-id="a4185-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="a4185-113">RemoveAt (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="a4185-114">Método SetAt</span><span class="sxs-lookup"><span data-stu-id="a4185-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="a4185-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4185-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="a4185-116">Append (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-116">Append Method</span></span>

<span data-ttu-id="a4185-117">Anexa un objeto al final de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="a4185-118">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="a4185-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-119">**Description**</span></span>

<span data-ttu-id="a4185-120">Al final de la colección, este método anexa un objeto que se pasa en la lista de parámetros, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4185-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![una figura que muestra cómo Append agrega una entrada a la colección](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="a4185-122">GetAt (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-122">GetAt Method</span></span>

<span data-ttu-id="a4185-123">Obtiene un objeto de una ubicación especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="a4185-124">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="a4185-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-125">**Description**</span></span>

<span data-ttu-id="a4185-126">Escribe el objeto almacenado en la ubicación de la colección especificada por el *Índice* en la variable a la que hace referencia el *objeto*.</span><span class="sxs-lookup"><span data-stu-id="a4185-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="a4185-127">Esta acción no cambia el contenido de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="a4185-128">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4185-128">The following diagram illustrates this process.</span></span>

![una figura que muestra cómo getadt recupera una entrada de la colección.](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="a4185-130">Método GetCount</span><span class="sxs-lookup"><span data-stu-id="a4185-130">GetCount Method</span></span>

<span data-ttu-id="a4185-131">Obtiene el número de objetos almacenados en la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="a4185-132">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="a4185-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-133">**Description**</span></span>

<span data-ttu-id="a4185-134">Escribe el número de objetos que están almacenados actualmente en la colección en la variable a la que hace referencia el *recuento*.</span><span class="sxs-lookup"><span data-stu-id="a4185-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="a4185-135">Esta acción no cambia el contenido de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="a4185-136">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4185-136">The following diagram illustrates this process.</span></span>

![una figura que muestra cómo getCount obtiene el número de entradas de la colección.](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="a4185-138">Método Insertat (</span><span class="sxs-lookup"><span data-stu-id="a4185-138">InsertAt Method</span></span>

<span data-ttu-id="a4185-139">Inserta un objeto en la ubicación especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="a4185-140">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="a4185-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-141">**Description**</span></span>

<span data-ttu-id="a4185-142">El objeto que se pasa en el *objeto* se inserta en la colección en la ubicación especificada por *index*.</span><span class="sxs-lookup"><span data-stu-id="a4185-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="a4185-143">Antes de insertar el nuevo *objeto*, este método se mueve por 1 el objeto que ha ocupado previamente la ubicación en el *Índice* y mueve todos los punteros de interfaz después al *Índice*.</span><span class="sxs-lookup"><span data-stu-id="a4185-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="a4185-144">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4185-144">The following diagram illustrates this process.</span></span>

![una figura que muestra cómo insertat (agrega una entrada a la colección](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="a4185-146">RemoveAt (método)</span><span class="sxs-lookup"><span data-stu-id="a4185-146">RemoveAt Method</span></span>

<span data-ttu-id="a4185-147">Quita el objeto de una ubicación especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="a4185-148">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="a4185-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-149">**Description**</span></span>

<span data-ttu-id="a4185-150">Este método libera el objeto de la ubicación especificada por el *Índice* y, a continuación, compacta la colección reduciendo en 1 el índice de cada puntero después del *Índice*.</span><span class="sxs-lookup"><span data-stu-id="a4185-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="a4185-151">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4185-151">The following diagram illustrates this process.</span></span>

![una figura que muestra cómo RemoveAt quita una entrada de la colección.](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="a4185-153">Método SetAt</span><span class="sxs-lookup"><span data-stu-id="a4185-153">SetAt Method</span></span>

<span data-ttu-id="a4185-154">Reemplaza el objeto situado en una ubicación especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4185-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="a4185-155">**Sintaxis genérica**</span><span class="sxs-lookup"><span data-stu-id="a4185-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="a4185-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a4185-156">**Description**</span></span>

<span data-ttu-id="a4185-157">Este método libera primero el objeto en la ubicación a la que hace referencia el *Índice* y, a continuación, reemplaza ese objeto por el que se pasa en el *objeto*.</span><span class="sxs-lookup"><span data-stu-id="a4185-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="a4185-158">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4185-158">The following diagram illustrates this process.</span></span>

![una figura que muestra cómo setat reemplaza una entrada en la colección](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="a4185-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4185-160">See Also</span></span>

<dl>

[<span data-ttu-id="a4185-161">**IXpsOMColorProfileResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="a4185-162">**IXpsOMDashCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="a4185-163">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="a4185-164">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="a4185-165">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="a4185-166">**IXpsOMGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="a4185-167">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="a4185-168">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="a4185-169">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="a4185-170">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="a4185-171">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="a4185-172">**IXpsOMSignatureBlockResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="a4185-173">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="a4185-174">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="a4185-175">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="a4185-176">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="a4185-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



