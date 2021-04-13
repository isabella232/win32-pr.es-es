---
description: 'Para que una aplicación de Tablet PC funcione con la entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Escenarios de interoperabilidad importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648175"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="3ef5f-103">Escenarios de interoperabilidad importantes</span><span class="sxs-lookup"><span data-stu-id="3ef5f-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="3ef5f-104">Para que una aplicación de Tablet PC funcione con la entrada de lápiz de forma eficaz, esa aplicación debe ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="3ef5f-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="3ef5f-105">Guarde un documento en el formato binario nativo de la aplicación sin perder la tinta del documento.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="3ef5f-106">Guardar un documento en cualquier formato que la aplicación admita normalmente (por ejemplo, HTML o formato de texto enriquecido (RTF)) sin perder la tinta del documento.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="3ef5f-107">Copiar la entrada manuscrita de una aplicación a otra mediante el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="3ef5f-108">Esto funciona si la otra aplicación solo reconoce un formato específico, como HTML, RTF o mapa de bits (BMP).</span><span class="sxs-lookup"><span data-stu-id="3ef5f-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="3ef5f-109">También funciona si la aplicación de destino reconoce la tinta.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="3ef5f-110">Si reconoce la tinta, la aplicación de destino puede interpretar la tinta que se ha copiado como tinta y no solo como una imagen.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="3ef5f-111">Copiar la entrada manuscrita, junto con el texto, entre dos aplicaciones que reconocen la tinta, cada una de las cuales tiene más de un objeto de [**entrada de lápiz**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef5f-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="3ef5f-112">Esto requiere HTML, RTF o un formato similar.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="3ef5f-113">Copie la entrada manuscrita entre dos aplicaciones, cada una de las cuales tiene un objeto de [**entrada manuscrita**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef5f-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="3ef5f-114">El formato serializado de tinta (ISF) es suficiente para esto.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="3ef5f-115">Copiar la entrada manuscrita de una aplicación que tiene más de un objeto de [**entrada de lápiz**](inkdisp-class.md) en una aplicación que solo tiene un objeto de **entrada manuscrita** .</span><span class="sxs-lookup"><span data-stu-id="3ef5f-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="3ef5f-116">En este caso, la aplicación que tiene más de un objeto de **entrada de lápiz** debe ser capaz de generar el formato serializado de tinta (ISF).</span><span class="sxs-lookup"><span data-stu-id="3ef5f-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="3ef5f-117">Copiar la entrada manuscrita de una aplicación que tiene un objeto de [**entrada manuscrita**](inkdisp-class.md) en una aplicación que tiene más de un objeto de **entrada manuscrita** .</span><span class="sxs-lookup"><span data-stu-id="3ef5f-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="3ef5f-118">En este caso, la aplicación que tiene más de un objeto de **entrada de lápiz** debe ser capaz de reconocer el ISF.</span><span class="sxs-lookup"><span data-stu-id="3ef5f-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



