---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fada27e903c465f9b5e0342fca481e5161b699c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678142"
---
# <a name="t-windows-installer"></a><span data-ttu-id="4dd1e-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="4dd1e-103">T (Windows Installer)</span></span>

<span data-ttu-id="4dd1e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [o](o-gly.md) [p](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [s](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="4dd1e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4dd1e-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**procesamiento de transacciones**</span><span class="sxs-lookup"><span data-stu-id="4dd1e-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="4dd1e-106">Una o varias operaciones procesadas juntas como un único entero indivisible denominado transacción.</span><span class="sxs-lookup"><span data-stu-id="4dd1e-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="4dd1e-107">Todas las operaciones constituyentes deben realizarse correctamente para que la transacción se realice correctamente; de lo contrario, todas las operaciones se revierten al estado original.</span><span class="sxs-lookup"><span data-stu-id="4dd1e-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="4dd1e-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transformación**</span><span class="sxs-lookup"><span data-stu-id="4dd1e-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="4dd1e-109">Plantilla de las diferencias entre dos [*bases de datos de instalador*](i-gly.md) que se pueden aplicar para producir cambios similares en otras bases de datos.</span><span class="sxs-lookup"><span data-stu-id="4dd1e-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="4dd1e-110">Por ejemplo, se puede usar una transformación de localización para cambiar el idioma de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dd1e-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="4dd1e-111">Para obtener más información, vea [combinaciones y transformaciones](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4dd1e-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dd1e-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**marcas de condición de error de transformación**</span><span class="sxs-lookup"><span data-stu-id="4dd1e-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="4dd1e-113">Conjunto de propiedades que se usan para marcar las condiciones de error de una [*transformación*](/windows).</span><span class="sxs-lookup"><span data-stu-id="4dd1e-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="4dd1e-114">Para obtener más información, vea [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="4dd1e-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="4dd1e-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transformar marcas de validación**</span><span class="sxs-lookup"><span data-stu-id="4dd1e-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="4dd1e-116">Conjunto de propiedades que se usan para comprobar que la [*transformación*](/windows) se puede aplicar a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4dd1e-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="4dd1e-117">Para obtener una lista de estas propiedades, vea [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="4dd1e-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
