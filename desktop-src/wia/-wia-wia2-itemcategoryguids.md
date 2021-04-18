---
description: Los elementos de adquisición de imágenes de Windows (WIA) 2,0 se agrupan en categorías que definen cómo se trata o se usa un IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID de categoría de elemento de WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715170"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="f282f-103">GUID de categoría de elemento de WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="f282f-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="f282f-104">Los elementos de adquisición de imágenes de Windows (WIA) 2,0 se agrupan en categorías que definen cómo se trata o se usa un [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="f282f-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="f282f-105">Por ejemplo, si el elemento representa un alimentador, la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="f282f-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="f282f-106">Si el elemento representa un archivo terminado, una aplicación WIA 2,0 debe tratarlo de este modo, suponiendo que los datos son estáticos y se encuentran en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f282f-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="f282f-107">(Las reglas de cada elemento se definirán en sus documentos de especificación individuales). Cada categoría tiene una constante de tipo GUID.</span><span class="sxs-lookup"><span data-stu-id="f282f-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="f282f-108">Constante</span><span class="sxs-lookup"><span data-stu-id="f282f-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="f282f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f282f-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="f282f-110"><dt>**Categoría de WIA \_ \_ auto**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="f282f-111">Un elemento que representa la configuración automática para un dispositivo de escáner WIA 2,0 que admite el análisis configurado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f282f-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="f282f-112"><dt>**\_alimentador de categoría WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="f282f-113">Un elemento del alimentador que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir los alimentadores de documentos.</span><span class="sxs-lookup"><span data-stu-id="f282f-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="f282f-114"><dt>**\_alimentador de categoría WIA \_ \_ atrás**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="f282f-115">Origen de datos programable que describe el origen de datos de la parte posterior de un elemento de alimentador de base dúplex.</span><span class="sxs-lookup"><span data-stu-id="f282f-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="f282f-116"><dt>**\_alimentador de categoría WIA \_ \_ delantero**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="f282f-117">Origen de datos programable que describe el origen de datos de front-end de un elemento de alimentador de base dúplex.</span><span class="sxs-lookup"><span data-stu-id="f282f-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="f282f-118"><dt>**\_película de categoría WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="f282f-119">Un elemento de película que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir las unidades de análisis de películas.</span><span class="sxs-lookup"><span data-stu-id="f282f-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="f282f-120"><dt>**archivo de categoría de WIA \_ \_ finalizada \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="f282f-121">Un elemento que no es un origen de datos programable, o un elemento que proporciona los datos en un formato de archivo terminado, o un elemento de carpeta que contiene los elementos de formato de archivo finalizados.</span><span class="sxs-lookup"><span data-stu-id="f282f-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="f282f-122"><dt>**plano de la \_ categoría WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="f282f-123">Un elemento plano que es un origen de datos programable y sigue las reglas estándar y los conjuntos de propiedades necesarios para admitir el análisis de placas de plano.</span><span class="sxs-lookup"><span data-stu-id="f282f-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="f282f-124"><dt>**\_carpeta de categoría WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="f282f-125">Elemento de almacenamiento en carpetas (no es un origen de datos programable) que contiene otros elementos de carpeta o archivos finalizados o ambos.</span><span class="sxs-lookup"><span data-stu-id="f282f-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="f282f-126"><dt>**raíz de la \_ categoría WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="f282f-127">Elemento raíz para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f282f-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="f282f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f282f-128">Requirements</span></span>



| <span data-ttu-id="f282f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f282f-129">Requirement</span></span> | <span data-ttu-id="f282f-130">Value</span><span class="sxs-lookup"><span data-stu-id="f282f-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f282f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f282f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f282f-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f282f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f282f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f282f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f282f-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f282f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f282f-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f282f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f282f-136"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="f282f-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




