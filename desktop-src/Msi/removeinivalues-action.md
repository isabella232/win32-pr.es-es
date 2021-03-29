---
description: La acción RemoveIniValues quita la información del archivo. ini especificada para su eliminación en la tabla RemoveIniFile si el componente está configurado para instalarse localmente o ejecutar desde el origen.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Acción RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002971"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="82286-103">Acción RemoveIniValues</span><span class="sxs-lookup"><span data-stu-id="82286-103">RemoveIniValues Action</span></span>

<span data-ttu-id="82286-104">La acción RemoveIniValues quita la información del archivo. ini especificada para su eliminación en la [tabla RemoveIniFile](removeinifile-table.md) si el componente está configurado para instalarse localmente o ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="82286-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="82286-105">La acción RemoveIniValues quita la información del archivo. ini que se ha asociado a un componente de la [tabla inifile](inifile-table.md).</span><span class="sxs-lookup"><span data-stu-id="82286-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="82286-106">Esta acción también quita la información del archivo. ini si la [acción WriteIniValues](writeinivalues-action.md) escribió la información y el componente está programado para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="82286-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="82286-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="82286-107">Sequence Restrictions</span></span>

<span data-ttu-id="82286-108">Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de la acción RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="82286-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="82286-109">Si se usa una acción [WriteIniValues](writeinivalues-action.md) en la secuencia, debe aparecer después de RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="82286-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="82286-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="82286-110">ActionData Messages</span></span>



| <span data-ttu-id="82286-111">Campo</span><span class="sxs-lookup"><span data-stu-id="82286-111">Field</span></span> | <span data-ttu-id="82286-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="82286-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="82286-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="82286-113">\[1\]</span></span> | <span data-ttu-id="82286-114">Identificador del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="82286-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="82286-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="82286-115">\[2\]</span></span> | <span data-ttu-id="82286-116">Una sección de la clave del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="82286-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="82286-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="82286-117">\[3\]</span></span> | <span data-ttu-id="82286-118">Elemento quitado del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="82286-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="82286-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="82286-119">\[4\]</span></span> | <span data-ttu-id="82286-120">Valor quitado del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="82286-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82286-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82286-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82286-122">Tabla RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="82286-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="82286-123">Tabla IniFile</span><span class="sxs-lookup"><span data-stu-id="82286-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="82286-124">Acción WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="82286-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="82286-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="82286-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



