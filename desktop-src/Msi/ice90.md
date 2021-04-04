---
description: ICE90 publica una advertencia si detecta que se ha especificado el directorio de un acceso directo como una propiedad pública.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908842"
---
# <a name="ice90"></a><span data-ttu-id="3f888-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="3f888-103">ICE90</span></span>

<span data-ttu-id="3f888-104">ICE90 publica una advertencia si detecta que se ha especificado el directorio de un acceso directo como una propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="3f888-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="3f888-105">Los nombres de [las propiedades públicas](public-properties.md) se escriben en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="3f888-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="3f888-106">Un acceso directo especificado por una propiedad pública puede no funcionar si cambia el valor de la propiedad [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="3f888-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="3f888-107">Esta acción personalizada de ICE valida la tabla de acceso directo y usa la tabla de directorio.</span><span class="sxs-lookup"><span data-stu-id="3f888-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="3f888-108">Si la tabla del directorio no está presente, devuelve sin validar la tabla de accesos directos y no envía ningún error ni ADVERTENCIA.</span><span class="sxs-lookup"><span data-stu-id="3f888-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="3f888-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="3f888-109">Result</span></span>

<span data-ttu-id="3f888-110">ICE90 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="3f888-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="3f888-111">Error ICE90</span><span class="sxs-lookup"><span data-stu-id="3f888-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="3f888-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f888-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="3f888-113">El acceso directo ' \[ 1 \] ' tiene un directorio que es una propiedad pública (todos los extremos) y está en el directorio del perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f888-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="3f888-114">Esto produce un problema si el valor de la propiedad [**AllUsers**](allusers.md) cambia en la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f888-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="3f888-115">El directorio de un acceso directo se ha especificado como una propiedad pública.</span><span class="sxs-lookup"><span data-stu-id="3f888-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="3f888-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f888-116">Example</span></span>

<span data-ttu-id="3f888-117">ICE90 notifica la siguiente advertencia para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3f888-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="3f888-118">En este ejemplo, MYDIR está en un perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="3f888-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="3f888-119">ICE90 publica una advertencia porque la ubicación del directorio de destino se especifica mediante una propiedad pública, MYDIR.</span><span class="sxs-lookup"><span data-stu-id="3f888-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="3f888-120">Un usuario puede cambiar MYDIR o la propiedad [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="3f888-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="3f888-121">Si se establece **AllUsers** para el [contexto de instalación](installation-context.md)por equipo y MYDIR está en un perfil de usuario, el archivo de acceso directo de MYDIR se copia en el perfil "todos los usuarios" y no en el perfil de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="3f888-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="3f888-122">Si se establece **AllUsers** para el contexto de instalación por usuario, el archivo de acceso directo de MYDIR se copia en el perfil de un usuario determinado y no está disponible para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="3f888-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="3f888-123">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f888-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="3f888-124">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="3f888-124">Shortcut</span></span>  | <span data-ttu-id="3f888-125">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="3f888-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="3f888-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="3f888-126">Shortcut1</span></span> | <span data-ttu-id="3f888-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="3f888-127">MYDIR</span></span>       |



 

<span data-ttu-id="3f888-128">[Tabla de directorio](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3f888-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="3f888-129">Directorio</span><span class="sxs-lookup"><span data-stu-id="3f888-129">Directory</span></span> | <span data-ttu-id="3f888-130">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="3f888-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="3f888-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="3f888-131">MYDIR</span></span>     | <span data-ttu-id="3f888-132">ProgramMenuFolder</span><span class="sxs-lookup"><span data-stu-id="3f888-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3f888-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f888-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f888-134">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3f888-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



