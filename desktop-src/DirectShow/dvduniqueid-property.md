---
description: La propiedad DVDUniqueID recupera un número generado por el sistema que identifica de forma única el disco actual.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propiedad DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906628"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="12309-103">Propiedad DVDUniqueID</span><span class="sxs-lookup"><span data-stu-id="12309-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="12309-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="12309-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="12309-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="12309-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="12309-106">La `DVDUniqueID` propiedad recupera un número generado por el sistema que identifica de forma única el disco actual.</span><span class="sxs-lookup"><span data-stu-id="12309-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="12309-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12309-107">Return Value</span></span>

<span data-ttu-id="12309-108">Devuelve un valor entero que identifica de forma única el disco actual.</span><span class="sxs-lookup"><span data-stu-id="12309-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="12309-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12309-109">Remarks</span></span>

<span data-ttu-id="12309-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="12309-110">This property is read-only with no default value.</span></span> <span data-ttu-id="12309-111">El número de identificación (ID.) no es absolutamente único, pero es único para todos los propósitos prácticos.</span><span class="sxs-lookup"><span data-stu-id="12309-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="12309-112">El identificador se aplica a todas las copias replicadas de un disco. En otras palabras, todas las copias de una película específica tienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="12309-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="12309-113">El identificador se basa en tamaños de archivo, fechas y otra información, y no en el valor de BCA.</span><span class="sxs-lookup"><span data-stu-id="12309-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



