---
description: La implementación de esta interfaz se proporciona como código de ejemplo con el SDK de DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interfaz IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677067"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="ef265-103">Interfaz IMpeg2PsiParser</span><span class="sxs-lookup"><span data-stu-id="ef265-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="ef265-104">La implementación de esta interfaz se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ef265-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="ef265-105">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="ef265-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="ef265-106">La `IMpeg2PsiParser` interfaz recupera información específica del programa (PSI) del filtro del analizador de PSI, que se proporciona en el SDK de DirectShow como filtro de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ef265-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="ef265-107">Una aplicación puede usar este filtro para asignar identificadores de programa (PID) en el filtro de demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="ef265-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="ef265-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef265-108">Members</span></span>

<span data-ttu-id="ef265-109">La interfaz **IMpeg2PsiParser** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ef265-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ef265-110">**IMpeg2PsiParser** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ef265-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="ef265-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef265-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef265-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef265-112">Methods</span></span>

<span data-ttu-id="ef265-113">La interfaz **IMpeg2PsiParser** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ef265-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="ef265-114">Método</span><span class="sxs-lookup"><span data-stu-id="ef265-114">Method</span></span>                                                                             | <span data-ttu-id="ef265-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef265-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef265-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef265-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="ef265-117">Busca el PID de la tabla de mapa de programas (PMT) para un programa, según el número de programa.</span><span class="sxs-lookup"><span data-stu-id="ef265-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="ef265-118">**GetCountOfElementaryStreams**</span><span class="sxs-lookup"><span data-stu-id="ef265-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="ef265-119">Recupera el número de flujos elementales en un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="ef265-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="ef265-120">**GetCountOfPrograms**</span><span class="sxs-lookup"><span data-stu-id="ef265-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="ef265-121">Recupera el número de programas en el flujo de transporte.</span><span class="sxs-lookup"><span data-stu-id="ef265-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="ef265-122">**GetPatVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="ef265-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="ef265-123">Recupera el \_ campo de número de versión de la tabla de Asociación de programas (PAT).</span><span class="sxs-lookup"><span data-stu-id="ef265-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="ef265-124">**GetPmtVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="ef265-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="ef265-125">Recupera el \_ campo de número de versión de un valor de PMT especificado.</span><span class="sxs-lookup"><span data-stu-id="ef265-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="ef265-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef265-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="ef265-127">Recupera la asignación de PID para una secuencia elemental especificada en un programa.</span><span class="sxs-lookup"><span data-stu-id="ef265-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="ef265-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef265-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="ef265-129">Recupera la asignación de PID para un objeto PMT especificado.</span><span class="sxs-lookup"><span data-stu-id="ef265-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="ef265-130">**GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="ef265-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="ef265-131">Recupera el número de programa para un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="ef265-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="ef265-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef265-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="ef265-133">Recupera el tipo de secuencia de una secuencia elemental especificada en un programa.</span><span class="sxs-lookup"><span data-stu-id="ef265-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="ef265-134">**GetTransportStreamId**</span><span class="sxs-lookup"><span data-stu-id="ef265-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="ef265-135">Recupera el \_ \_ campo de identificador de flujo de transporte de la Pat.</span><span class="sxs-lookup"><span data-stu-id="ef265-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="ef265-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef265-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef265-137">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="ef265-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
