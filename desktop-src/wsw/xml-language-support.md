---
title: Compatibilidad con el lenguaje XML
description: En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Compatibilidad del lenguaje XML con servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105665889"
---
# <a name="xml-language-support"></a><span data-ttu-id="41004-106">Compatibilidad con el lenguaje XML</span><span class="sxs-lookup"><span data-stu-id="41004-106">XML Language Support</span></span>

<span data-ttu-id="41004-107">En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.</span><span class="sxs-lookup"><span data-stu-id="41004-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="41004-108">Vea las funciones DownlevelLCIDToLocaleName en versiones de Windows anteriores a Windows Vista y LCIDToLocalName en caso contrario, para realizar la conversión entre un LCID y un valor XML: lang.</span><span class="sxs-lookup"><span data-stu-id="41004-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="41004-109">Al leer, se puede usar [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) para detectar el valor de un atributo "XML: lang" en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="41004-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="41004-110">Al escribir, se puede usar [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) para escribir un atributo "XML: lang".</span><span class="sxs-lookup"><span data-stu-id="41004-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




