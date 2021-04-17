---
description: La propiedad ColumnInfo del objeto de vista devuelve un objeto de registro que contiene la información solicitada sobre cada columna del conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653551"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="011ff-103">View. ColumnInfo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="011ff-103">View.ColumnInfo property</span></span>

<span data-ttu-id="011ff-104">La propiedad **ColumnInfo** del objeto de [**vista**](view-object.md) devuelve un objeto de [**registro**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="011ff-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="011ff-105">Es posible que se soliciten los nombres de columna o las definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="011ff-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="011ff-106">Las constantes que se proporcionan en la lista de selección no tienen nombres.</span><span class="sxs-lookup"><span data-stu-id="011ff-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="011ff-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="011ff-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="011ff-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="011ff-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="011ff-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="011ff-109">Property value</span></span>

<span data-ttu-id="011ff-110">Información necesaria necesaria para cada columna.</span><span class="sxs-lookup"><span data-stu-id="011ff-110">Required information needed for each column.</span></span>



| <span data-ttu-id="011ff-111">Nombre de parámetro</span><span class="sxs-lookup"><span data-stu-id="011ff-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="011ff-112">Significado</span><span class="sxs-lookup"><span data-stu-id="011ff-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="011ff-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="011ff-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="011ff-114">Devuelve los nombres de todas las columnas no constantes en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="011ff-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="011ff-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="011ff-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="011ff-116">Devuelve los tipos de todas las columnas no constantes en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="011ff-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="011ff-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="011ff-117">Remarks</span></span>

<span data-ttu-id="011ff-118">Las descripciones de columna devueltas por la propiedad **ColumnInfo** tienen el formato que se describe en [formato de definición de columna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="011ff-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="011ff-119">Cada columna se describe mediante una cadena en el campo registro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="011ff-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="011ff-120">La cadena de definición se compone de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres si es aplicable, o en bytes).</span><span class="sxs-lookup"><span data-stu-id="011ff-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="011ff-121">Un ancho de cero designa un ancho sin enlazar (campos de texto largo y secuencias).</span><span class="sxs-lookup"><span data-stu-id="011ff-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="011ff-122">Una letra mayúscula indica que se permiten valores NULL en la columna.</span><span class="sxs-lookup"><span data-stu-id="011ff-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="011ff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011ff-123">Requirements</span></span>



| <span data-ttu-id="011ff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="011ff-124">Requirement</span></span> | <span data-ttu-id="011ff-125">Value</span><span class="sxs-lookup"><span data-stu-id="011ff-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="011ff-126">Versión</span><span class="sxs-lookup"><span data-stu-id="011ff-126">Version</span></span><br/> | <span data-ttu-id="011ff-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="011ff-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="011ff-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="011ff-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="011ff-129">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="011ff-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="011ff-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="011ff-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="011ff-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="011ff-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="011ff-132">IID</span><span class="sxs-lookup"><span data-stu-id="011ff-132">IID</span></span><br/>     | <span data-ttu-id="011ff-133">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="011ff-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




