---
description: La versión de PATCHWIZ.DLL publicada con Windows Installer&\# 160; 3.0 puede generar automáticamente información de secuencia de revisiones y agregar a la tabla MsiPatchSequence una nueva revisión.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generando información de secuencia de revisión (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002262"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="e7920-103">Generando información de secuencia de revisión (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="e7920-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="e7920-104">La versión de [PATCHWIZ.DLL](patchwiz-dll.md) publicada con Windows Installer 3,0 puede generar automáticamente información de secuencia de revisiones y agregar a la [tabla MsiPatchSequence](msipatchsequence-table.md) una nueva revisión.</span><span class="sxs-lookup"><span data-stu-id="e7920-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="e7920-105">Establezca la \_ propiedad secuencia \_ \_ de generación de datos deshabilitada en 1 (uno) en la [tabla de propiedades](properties-table-patchwiz-dll-.md) del archivo. PCP para evitar la generación automática de información sobre la secuenciación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="e7920-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="e7920-106">Si esta propiedad no está presente, la información se genera y se agrega automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e7920-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="e7920-107">Cuando se utiliza el [PATCHWIZ.DLL](patchwiz-dll.md) liberado con Windows Installer 3,0 para generar automáticamente la información de secuenciación de revisiones, ocurre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e7920-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="e7920-108">Se agrega una nueva fila a la [tabla MsiPatchSequence](msipatchsequence-table.md) para cada código de producto de una imagen de destino que aparece en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="e7920-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="e7920-109">Los valores agregados a la columna PatchFamily en las nuevas filas corresponden a los códigos de producto de destino de las imágenes de destino que se enumeran en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="e7920-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="e7920-110">Los valores agregados a las columnas de secuencia en las nuevas filas se generan con la versión de producto más alta de destino de la revisión y la hora UTC en que se genera la revisión.</span><span class="sxs-lookup"><span data-stu-id="e7920-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="e7920-111">El número de secuencia es <Product Minor Version> . <Build Major Number> . <marca de tiempo 1>. <la marca de tiempo 2>.</span><span class="sxs-lookup"><span data-stu-id="e7920-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="e7920-112">El primer campo es la versión del producto de la versión más reciente del producto que es el destino de la revisión.</span><span class="sxs-lookup"><span data-stu-id="e7920-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="e7920-113">El segundo campo es el número principal de la compilación de la versión más reciente del producto que es el destino de la revisión.</span><span class="sxs-lookup"><span data-stu-id="e7920-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="e7920-114">Los dos campos de marca de tiempo tienen en cuenta la marca de tiempo de 32 bits necesaria para contar los segundos en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="e7920-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="e7920-115">Las versiones del producto tienen el siguiente formato: <Product Major Version> . <Product Minor Version> .. <Build Major Number> <Build Minor Number> y un producto con un número de versión 2.1.0.0 es una versión superior a un producto con el número de versión 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="e7920-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="e7920-116">El atributo msidbPatchSequenceSupersedeEarlier se especifica en la columna de atributos de las nuevas filas que se generan para Service Packs (SP) o revisiones de actualización secundarias.</span><span class="sxs-lookup"><span data-stu-id="e7920-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="e7920-117">El atributo msidbPatchSequenceSupersedeEarlier no se agrega a una revisión de actualización pequeña o QFE.</span><span class="sxs-lookup"><span data-stu-id="e7920-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="e7920-118">Un Service Pack (SP) debe contener las correcciones de todas las QFE publicadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e7920-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="e7920-119">Sin embargo, si el autor de una revisión establece la propiedad de sustitución de datos de secuencia \_ \_ en 0 (cero) o 1 (uno) en el archivo. PCP, la columna atributos de todas las filas de la tabla MsiPatchSequence se establece en el valor que se especifica para la sustitución de datos de secuencia \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7920-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="e7920-120">Los autores de revisiones que requieren más control deben crear manualmente la columna de atributos.</span><span class="sxs-lookup"><span data-stu-id="e7920-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="e7920-121">Si incluye una [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) en el archivo. PCP, \_ \_ se omite la propiedad generación de datos de secuencia \_ deshabilitada y se puede Agregar la información proporcionada en la tabla PatchSequence a la [tabla MsiPatchSequence](msipatchsequence-table.md) de la revisión.</span><span class="sxs-lookup"><span data-stu-id="e7920-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



