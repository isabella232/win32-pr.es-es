---
description: Una aplicación usa las siguientes interfaces para administrar el paquete de documentos impresos.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Interfaces de la API del paquete de documentos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697611"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="9f074-103">Interfaces de la API del paquete de documentos de impresión</span><span class="sxs-lookup"><span data-stu-id="9f074-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="9f074-104">Una aplicación usa las siguientes interfaces para administrar el paquete de documentos impresos.</span><span class="sxs-lookup"><span data-stu-id="9f074-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9f074-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9f074-105">In this section</span></span>



| <span data-ttu-id="9f074-106">Tema</span><span class="sxs-lookup"><span data-stu-id="9f074-106">Topic</span></span>                                                                                       | <span data-ttu-id="9f074-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f074-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f074-108">**IPrintDocumentPackageStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="9f074-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="9f074-109">Representa el progreso del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="9f074-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="9f074-110">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="9f074-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="9f074-111">Permite a los usuarios enumerar los tipos de destino del paquete compatible y crear uno con un identificador de tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="9f074-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="9f074-112">**IPrintDocumentPackageTarget** también admite el seguimiento del progreso de la impresión del paquete y la cancelación.</span><span class="sxs-lookup"><span data-stu-id="9f074-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="9f074-113">**IPrintDocumentPackageTargetFactory**</span><span class="sxs-lookup"><span data-stu-id="9f074-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="9f074-114">Se usa con [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para iniciar un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="9f074-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

