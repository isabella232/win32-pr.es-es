---
description: La acción WriteIniValues escribe la información del archivo. ini que la aplicación necesita escribir en sus archivos. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Acción WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910666"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="88e95-103">Acción WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="88e95-103">WriteIniValues Action</span></span>

<span data-ttu-id="88e95-104">La acción WriteIniValues escribe la información del archivo. ini que la aplicación necesita escribir en sus archivos. ini.</span><span class="sxs-lookup"><span data-stu-id="88e95-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="88e95-105">La escritura de esta información se valida mediante la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="88e95-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="88e95-106">Se escribe un valor. ini si se ha establecido que el componente correspondiente se instale localmente o se ejecute desde el origen.</span><span class="sxs-lookup"><span data-stu-id="88e95-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="88e95-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="88e95-107">Sequence Restrictions</span></span>

<span data-ttu-id="88e95-108">La acción InstallValidate debe ser anterior a la acción WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="88e95-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="88e95-109">Si hay una [acción RemoveIniValues](removeinivalues-action.md) en la secuencia, debe ser anterior a la acción WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="88e95-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="88e95-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="88e95-110">ActionData Messages</span></span>



| <span data-ttu-id="88e95-111">Campo</span><span class="sxs-lookup"><span data-stu-id="88e95-111">Field</span></span> | <span data-ttu-id="88e95-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="88e95-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="88e95-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="88e95-113">\[1\]</span></span> | <span data-ttu-id="88e95-114">Identificador del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="88e95-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="88e95-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="88e95-115">\[2\]</span></span> | <span data-ttu-id="88e95-116">clave del archivo. ini en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="88e95-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="88e95-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="88e95-117">\[3\]</span></span> | <span data-ttu-id="88e95-118">Elemento quitado del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="88e95-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="88e95-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="88e95-119">\[4\]</span></span> | <span data-ttu-id="88e95-120">Valor quitado del archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="88e95-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="88e95-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88e95-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e95-122">Tabla IniFile</span><span class="sxs-lookup"><span data-stu-id="88e95-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



