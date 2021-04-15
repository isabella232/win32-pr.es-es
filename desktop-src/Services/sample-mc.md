---
description: A continuación se muestra un archivo de mensajes de ejemplo que se puede usar para crear un archivo DLL de solo recursos que se utilizará con el ejemplo de servicio al escribir eventos en el registro de eventos.
ms.assetid: d0d46041-5608-4abf-b833-7aae1744ef60
title: Sample.mc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b34c87fad27b08671de57d7e329073df5a48579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669724"
---
# <a name="samplemc"></a><span data-ttu-id="f3b69-103">Sample.mc</span><span class="sxs-lookup"><span data-stu-id="f3b69-103">Sample.mc</span></span>

<span data-ttu-id="f3b69-104">A continuación se muestra un archivo de mensajes de ejemplo que se puede usar para crear un archivo DLL de solo recursos que se utilizará con el ejemplo de servicio al escribir eventos en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="f3b69-104">The following is an example message file that can be used to build a resource-only DLL to be used with the service sample when writing events to the event log.</span></span>

<span data-ttu-id="f3b69-105">Siga estos pasos para compilar el archivo DLL:</span><span class="sxs-lookup"><span data-stu-id="f3b69-105">Use the following steps to build the DLL:</span></span>

1.  <span data-ttu-id="f3b69-106">**MC-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="f3b69-106">**mc -U sample.mc**</span></span>
2.  <span data-ttu-id="f3b69-107">**RC-r sample. RC**</span><span class="sxs-lookup"><span data-stu-id="f3b69-107">**rc -r sample.rc**</span></span>
3.  <span data-ttu-id="f3b69-108">**Link-dll-NOENTRY -out:sample.dll sample. res**</span><span class="sxs-lookup"><span data-stu-id="f3b69-108">**link -dll -noentry -out:sample.dll sample.res**</span></span>

``` syntax
MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
    Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
    Warning=0x2:STATUS_SEVERITY_WARNING
    Error=0x3:STATUS_SEVERITY_ERROR
    )


FacilityNames=(System=0x0:FACILITY_SYSTEM
    Runtime=0x2:FACILITY_RUNTIME
    Stubs=0x3:FACILITY_STUBS
    Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=SVC_ERROR
Language=English
An error has occurred (%2).
.

; // A message file must end with a period on its own line
; // followed by a blank line.
```

## <a name="related-topics"></a><span data-ttu-id="f3b69-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3b69-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b69-110">El ejemplo de servicio completo</span><span class="sxs-lookup"><span data-stu-id="f3b69-110">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



