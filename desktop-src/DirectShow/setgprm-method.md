---
description: El método SetGPRM establece el registro del parámetro general especificado en el valor especificado.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Método SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686320"
---
# <a name="setgprm-method"></a><span data-ttu-id="b95ca-103">Método SetGPRM</span><span class="sxs-lookup"><span data-stu-id="b95ca-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="b95ca-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b95ca-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b95ca-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b95ca-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b95ca-106">El `SetGPRM` método establece el registro del parámetro general especificado en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b95ca-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="b95ca-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b95ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b95ca-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="b95ca-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="b95ca-109">Especifica el registro de parámetros general que se va a establecer como un entero.</span><span class="sxs-lookup"><span data-stu-id="b95ca-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="b95ca-110">El valor entero debe oscilar entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="b95ca-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="b95ca-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*Nvalor*</span><span class="sxs-lookup"><span data-stu-id="b95ca-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="b95ca-112">Especifica el nuevo valor del registro como un entero.</span><span class="sxs-lookup"><span data-stu-id="b95ca-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b95ca-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b95ca-113">Remarks</span></span>

<span data-ttu-id="b95ca-114">Los registros de parámetros generales, o GPRMs, son registros de 16 bits que cada disco puede utilizar de manera única para el almacenamiento de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="b95ca-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="b95ca-115">Una aplicación de reproducción no necesita tener acceso a estos registros para cualquier control de navegación o reproducción estándar mediante el objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="b95ca-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="b95ca-116">Este método se proporciona para las aplicaciones de reproductor que implementan la funcionalidad avanzada.</span><span class="sxs-lookup"><span data-stu-id="b95ca-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="b95ca-117">No intente modificar el GPRMs directamente a menos que tenga un conocimiento exhaustivo de la especificación del DVD y las maneras en las que se usa el GPRMs en el disco determinado que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="b95ca-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="b95ca-118">Si se cambian estos valores, se puede producir un comportamiento impredecible.</span><span class="sxs-lookup"><span data-stu-id="b95ca-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



