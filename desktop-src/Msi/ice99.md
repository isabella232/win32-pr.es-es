---
description: ICE99 comprueba que ningún nombre de propiedad especificado en la tabla del directorio duplica un nombre reservado para el uso público o privado del Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814411"
---
# <a name="ice99"></a><span data-ttu-id="e151c-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="e151c-103">ICE99</span></span>

<span data-ttu-id="e151c-104">ICE99 comprueba que ningún nombre de propiedad especificado en la tabla del [directorio](directory-table.md) duplica un nombre reservado para el uso público o privado del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e151c-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="e151c-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="e151c-105">Result</span></span>

<span data-ttu-id="e151c-106">ICE99 expone el siguiente error.</span><span class="sxs-lookup"><span data-stu-id="e151c-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="e151c-107">Error ICE99</span><span class="sxs-lookup"><span data-stu-id="e151c-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="e151c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e151c-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e151c-109">El nombre del directorio: \[ 1 \] es el mismo que el de una de las propiedades públicas de MSI y puede producir efectos secundarios imprevistos.</span><span class="sxs-lookup"><span data-stu-id="e151c-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="e151c-110">El valor de la columna Directory de la tabla [Directory](directory-table.md) duplica un nombre de propiedad reservado por el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e151c-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="e151c-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e151c-111">Example</span></span>

<span data-ttu-id="e151c-112">ICE99 notifica el siguiente error para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e151c-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="e151c-113">[Directorio](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e151c-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="e151c-114">Directorio</span><span class="sxs-lookup"><span data-stu-id="e151c-114">Directory</span></span>        | <span data-ttu-id="e151c-115">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="e151c-115">Directory\_Parent</span></span> | <span data-ttu-id="e151c-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="e151c-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="e151c-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="e151c-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="e151c-118">Para corregir esta advertencia, debe cambiar el nombre de CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="e151c-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e151c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e151c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e151c-120">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="e151c-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="e151c-121">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="e151c-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="e151c-122">No se admite en Windows Installer 3,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e151c-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



