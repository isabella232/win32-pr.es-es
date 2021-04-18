---
description: En el visor de fotogramas Monitor de red se muestran los datos analizados en tres paneles.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Ver información analizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562758"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="e1037-103">Ver información analizada</span><span class="sxs-lookup"><span data-stu-id="e1037-103">Viewing Parsed Information</span></span>

<span data-ttu-id="e1037-104">En el visor de fotogramas Monitor de red se muestran los datos analizados en tres paneles.</span><span class="sxs-lookup"><span data-stu-id="e1037-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="e1037-105">En el panel superior se muestra un resumen del marco que incluye el protocolo identificado.</span><span class="sxs-lookup"><span data-stu-id="e1037-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="e1037-106">En el panel central se muestran las propiedades de los datos con formato que se pueden organizar jerárquicamente como parte de la presentación del analizador.</span><span class="sxs-lookup"><span data-stu-id="e1037-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="e1037-107">En el panel inferior se muestran los datos sin procesar resaltados que se seleccionan en el panel central.</span><span class="sxs-lookup"><span data-stu-id="e1037-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="e1037-108">Puede especificar cómo se muestra la información en el visor al desarrollar su propio analizador.</span><span class="sxs-lookup"><span data-stu-id="e1037-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="e1037-109">En la ilustración siguiente se muestra cómo se puede mostrar información en el visor de tramas de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="e1037-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![visor de tramas del monitor de red](images/parseui.png)

> [!Note]  
> <span data-ttu-id="e1037-111">Los analizadores no muestran fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e1037-111">Parsers do not display frames.</span></span> <span data-ttu-id="e1037-112">Los analizadores reconocen los campos en la información proporcionada y, a continuación, notifican a Monitor de red para mostrar el marco.</span><span class="sxs-lookup"><span data-stu-id="e1037-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="e1037-113">El filtrado es una operación de nivel superior que permite que las consultas de filtro abarquen los analizadores.</span><span class="sxs-lookup"><span data-stu-id="e1037-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="e1037-114">En el analizador, use solo funciones que se puedan ejecutar en aplicaciones de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="e1037-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="e1037-115">Antes de adjuntar propiedades a los datos sin procesar, un analizador debe registrar primero todas las propiedades posibles con el kernel Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="e1037-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="e1037-116">El analizador envía un mensaje al kernel para crear una base de datos de propiedades y, a continuación, rellena la base de datos de propiedades con cada propiedad posible para su Protocolo.</span><span class="sxs-lookup"><span data-stu-id="e1037-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="e1037-117">Cada propiedad de la base de datos de propiedades contiene información como, por ejemplo, una descripción textual, un tipo de datos y un calificador que se usan para dar formato a los datos sin procesar y una rutina de formato que se usa para mostrar los datos.</span><span class="sxs-lookup"><span data-stu-id="e1037-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



