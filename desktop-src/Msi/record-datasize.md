---
description: La propiedad Datasize del objeto Record es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propiedad record. Datasize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653676"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="a138c-103">Propiedad record. Datasize</span><span class="sxs-lookup"><span data-stu-id="a138c-103">Record.DataSize property</span></span>

<span data-ttu-id="a138c-104">La propiedad **datasize** del objeto [**Record**](record-object.md) es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado.</span><span class="sxs-lookup"><span data-stu-id="a138c-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="a138c-105">Si los datos son una secuencia, se devuelve la longitud de la secuencia en bytes.</span><span class="sxs-lookup"><span data-stu-id="a138c-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="a138c-106">Si los datos son una cadena, se devuelve la longitud de la cadena sin null.</span><span class="sxs-lookup"><span data-stu-id="a138c-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="a138c-107">Si los datos son un entero, se devuelve el valor 4 (que indica el tamaño del entero).</span><span class="sxs-lookup"><span data-stu-id="a138c-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="a138c-108">Si los datos son NULL, se devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="a138c-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="a138c-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a138c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a138c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a138c-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="a138c-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a138c-111">Property value</span></span>

<span data-ttu-id="a138c-112">Número de campo obligatorio del valor dentro del registro, basado en 1.</span><span class="sxs-lookup"><span data-stu-id="a138c-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="a138c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a138c-113">Requirements</span></span>



| <span data-ttu-id="a138c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a138c-114">Requirement</span></span> | <span data-ttu-id="a138c-115">Value</span><span class="sxs-lookup"><span data-stu-id="a138c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a138c-116">Versión</span><span class="sxs-lookup"><span data-stu-id="a138c-116">Version</span></span><br/> | <span data-ttu-id="a138c-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a138c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a138c-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a138c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a138c-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a138c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a138c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a138c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a138c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a138c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a138c-122">IID</span><span class="sxs-lookup"><span data-stu-id="a138c-122">IID</span></span><br/>     | <span data-ttu-id="a138c-123">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a138c-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




