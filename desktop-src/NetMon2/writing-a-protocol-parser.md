---
description: Este tema contiene información acerca de cómo escribir un analizador de protocolos e incluye ejemplos de las funciones de exportación que el archivo DLL del analizador debe implementar.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Escritura de un analizador de protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545003"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="c7119-103">Escritura de un analizador de protocolos</span><span class="sxs-lookup"><span data-stu-id="c7119-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="c7119-104">Este tema contiene información acerca de cómo escribir un analizador de protocolos e incluye ejemplos de las funciones de exportación que el archivo DLL del analizador debe implementar.</span><span class="sxs-lookup"><span data-stu-id="c7119-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="c7119-105">En esta sección se incluyen los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7119-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="c7119-106">Término</span><span class="sxs-lookup"><span data-stu-id="c7119-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="c7119-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7119-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7119-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Consideraciones de programación](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="c7119-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="c7119-109">Identifica las sugerencias de programación básicas que le ayudarán a escribir un archivo DLL de analizador.</span><span class="sxs-lookup"><span data-stu-id="c7119-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="c7119-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementar funciones de exportación de analizador](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="c7119-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="c7119-111">Proporciona ejemplos de implementación de funciones de exportación.</span><span class="sxs-lookup"><span data-stu-id="c7119-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="c7119-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Aplicar formato a los datos mostrados](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="c7119-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="c7119-113">Identifica el proceso de formato de los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="c7119-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="c7119-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Especificar un conjunto de seguimiento](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="c7119-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="c7119-115">Identifica el proceso de especificación de un conjunto de seguimiento y muestra cómo Monitor de red tiene acceso al siguiente conjunto de un analizador para determinar el protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7119-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="c7119-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Especificar un conjunto de entrega](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="c7119-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="c7119-117">Identifica el proceso de especificación de un conjunto de entregas y muestra cómo el analizador accede a su conjunto de entrega para obtener un identificador del protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7119-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




