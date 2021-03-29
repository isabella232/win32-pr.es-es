---
description: ICE81 valida la tabla MsiDigitalCertificate, la tabla MsiDigitalSignature, la tabla MsiPatchCertificate y la tabla MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810742"
---
# <a name="ice81"></a><span data-ttu-id="76b49-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="76b49-103">ICE81</span></span>

<span data-ttu-id="76b49-104">ICE81 valida la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md), la tabla [MsiDigitalSignature](msidigitalsignature-table.md), la tabla [MsiPatchCertificate](msipatchcertificate-table.md)y la [tabla MsiPackageCertificate](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="76b49-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="76b49-105">Esta acción personalizada de ICE publica advertencias para los certificados digitales que no se usan o a los que no se hace referencia, y envía un error cuando el objeto firmado no existe o cuando el archivo. cab del objeto firmado no apunta a datos externos.</span><span class="sxs-lookup"><span data-stu-id="76b49-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="76b49-106">Tenga en cuenta que ICE03 comprueba que la entrada de la columna de tabla de la tabla MsiDigitalSignature es "media".</span><span class="sxs-lookup"><span data-stu-id="76b49-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="76b49-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="76b49-107">Result</span></span>

<span data-ttu-id="76b49-108">ICE81 envía las siguientes advertencias para los certificados digitales no usados o sin referencia.</span><span class="sxs-lookup"><span data-stu-id="76b49-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="76b49-109">ADVERTENCIA de ICE81</span><span class="sxs-lookup"><span data-stu-id="76b49-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="76b49-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="76b49-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="76b49-111">No se encontró ninguna referencia a ninguno de los registros de la tabla MsiDigitalCertificate en las tablas MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="76b49-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="76b49-112">Se devuelve esta advertencia si no se utilizan todos los registros.</span><span class="sxs-lookup"><span data-stu-id="76b49-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="76b49-113">No se encontró ninguna referencia al certificado digital \[ 1 \] en las tablas MsiDigitalSignature, MsiPackageCertificate o MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="76b49-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="76b49-114">Se devuelve esta advertencia si no se usan algunos registros, pero no todos.</span><span class="sxs-lookup"><span data-stu-id="76b49-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="76b49-115">ICE81 expone los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="76b49-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="76b49-116">Error ICE81</span><span class="sxs-lookup"><span data-stu-id="76b49-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="76b49-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="76b49-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b49-118">La tabla de medios no existe.</span><span class="sxs-lookup"><span data-stu-id="76b49-118">Media Table does not exist.</span></span> <span data-ttu-id="76b49-119">Por lo tanto, todas las entradas de MsiDigitalSignature son incorrectas</span><span class="sxs-lookup"><span data-stu-id="76b49-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="76b49-120">El objeto firmado no existe.</span><span class="sxs-lookup"><span data-stu-id="76b49-120">The signed object does not exist.</span></span> <span data-ttu-id="76b49-121">Se devuelve este error si la tabla de medios no existe pero MsiDigitalSignature tiene entradas.</span><span class="sxs-lookup"><span data-stu-id="76b49-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="76b49-122">Falta el objeto con signo \[ 2 \] en la tabla de medios</span><span class="sxs-lookup"><span data-stu-id="76b49-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="76b49-123">El objeto con signo \[ 2 no \] existe.</span><span class="sxs-lookup"><span data-stu-id="76b49-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="76b49-124">Este error se devuelve si la tabla de medios existe, pero esta entrada en MsiDigitalSignature no está presente en la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="76b49-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="76b49-125">La entrada de la tabla \[ 1 \] con la clave \[ 2 \] está firmada.</span><span class="sxs-lookup"><span data-stu-id="76b49-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="76b49-126">Por lo tanto, el archivo. cab debe apuntar a un objeto fuera del paquete (el valor de Cabinet no debe ir precedido de \# )</span><span class="sxs-lookup"><span data-stu-id="76b49-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="76b49-127">El archivo. cab del objeto firmado no apunta a datos externos.</span><span class="sxs-lookup"><span data-stu-id="76b49-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="76b49-128">\[1 \] es el nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76b49-128">\[1\] is table name.</span></span> <span data-ttu-id="76b49-129">\[2 \] es la clave en la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="76b49-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="76b49-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76b49-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b49-131">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="76b49-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



