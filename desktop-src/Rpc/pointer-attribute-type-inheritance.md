---
title: Herencia de tipos de Pointer-Attribute
description: Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421230"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="78e8d-103">Herencia de tipos de Pointer-Attribute</span><span class="sxs-lookup"><span data-stu-id="78e8d-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="78e8d-104">Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros.</span><span class="sxs-lookup"><span data-stu-id="78e8d-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="78e8d-105">Si no se asigna un atributo explícito a un puntero, el puntero utiliza el valor especificado por la \[ palabra clave [ \_ default del puntero](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="78e8d-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="78e8d-106">Algunas implementaciones de DCE no permiten punteros sin atributos.</span><span class="sxs-lookup"><span data-stu-id="78e8d-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="78e8d-107">Si un puntero no tiene un atributo explícito, el archivo IDL debe tener una especificación **\[ \_ predeterminada \] de puntero** para que se pueda establecer el atributo de puntero.</span><span class="sxs-lookup"><span data-stu-id="78e8d-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="78e8d-108">En el modo predeterminado (extensiones de Microsoft), puede especificar el atributo de un puntero en el archivo IDL que importa el archivo de definición de IDL.</span><span class="sxs-lookup"><span data-stu-id="78e8d-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="78e8d-109">Los punteros definidos en un archivo IDL pueden heredar atributos que se especifican en otros archivos IDL.</span><span class="sxs-lookup"><span data-stu-id="78e8d-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="78e8d-110">Además, en el modo predeterminado, los archivos IDL pueden incluir punteros sin atributos.</span><span class="sxs-lookup"><span data-stu-id="78e8d-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="78e8d-111">Si ni la base ni los archivos IDL importados especifican un atributo de puntero o el **\[ \_ valor predeterminado \] de puntero**, los punteros sin atributos se interpretan como punteros únicos.</span><span class="sxs-lookup"><span data-stu-id="78e8d-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="78e8d-112">El compilador MIDL asigna atributos de puntero a punteros utilizando las siguientes reglas de prioridad (1 es la más alta).</span><span class="sxs-lookup"><span data-stu-id="78e8d-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="78e8d-113">Prioridad</span><span class="sxs-lookup"><span data-stu-id="78e8d-113">Priority</span></span> | <span data-ttu-id="78e8d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="78e8d-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e8d-115">1</span><span class="sxs-lookup"><span data-stu-id="78e8d-115">1</span></span>        | <span data-ttu-id="78e8d-116">Los atributos de puntero explícitos se aplican al puntero en la definición o el sitio de uso.</span><span class="sxs-lookup"><span data-stu-id="78e8d-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="78e8d-117">2</span><span class="sxs-lookup"><span data-stu-id="78e8d-117">2</span></span>        | <span data-ttu-id="78e8d-118">El valor predeterminado es el atributo **\[ \_ predeterminado \] del puntero** en el archivo IDL que define el tipo.</span><span class="sxs-lookup"><span data-stu-id="78e8d-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="78e8d-119">3</span><span class="sxs-lookup"><span data-stu-id="78e8d-119">3</span></span>        | <span data-ttu-id="78e8d-120">El valor predeterminado es el atributo **\[ \_ predeterminado \] del puntero** en el archivo IDL que importa el tipo.</span><span class="sxs-lookup"><span data-stu-id="78e8d-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="78e8d-121">4</span><span class="sxs-lookup"><span data-stu-id="78e8d-121">4</span></span>        | <span data-ttu-id="78e8d-122">El valor predeterminado es \[ [ptr](/windows/desktop/Midl/ptr) \] en modo de compatibilidad de DCE o \[ [único](/windows/desktop/Midl/unique) \] en el modo de extensiones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78e8d-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 