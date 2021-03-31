---
title: Tipo complejo de ChannelLoggingType
description: Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si son secuenciales o circulares. | Tipo complejo de ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157116"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="1f699-105">Tipo complejo de ChannelLoggingType</span><span class="sxs-lookup"><span data-stu-id="1f699-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="1f699-106">Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si son secuenciales o circulares.</span><span class="sxs-lookup"><span data-stu-id="1f699-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1f699-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f699-107">Child elements</span></span>



| <span data-ttu-id="1f699-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f699-108">Element</span></span>                                                                         | <span data-ttu-id="1f699-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f699-109">Type</span></span>                                                              | <span data-ttu-id="1f699-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f699-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f699-111">**Seguridad automatizada**</span><span class="sxs-lookup"><span data-stu-id="1f699-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="1f699-112">boolean</span><span class="sxs-lookup"><span data-stu-id="1f699-112">boolean</span></span>                                                           | <span data-ttu-id="1f699-113">Determina si se debe crear un nuevo archivo de registro cuando el archivo de registro actual alcanza su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="1f699-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="1f699-114">Establézcalo en **true** para solicitar que el servicio cree un nuevo archivo cuando el archivo de registro alcance su tamaño máximo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1f699-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="1f699-115">Puede establecer [**AutoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) en **true** solo si la [**retención**](eventmanifestschema-retention-channelloggingtype-element.md) está establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="1f699-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="1f699-116">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="1f699-116">The default is **false**.</span></span><br/> <span data-ttu-id="1f699-117">No hay ningún límite en cuanto al número de archivos de copia de seguridad que puede crear el servicio (limitado solo por el espacio en disco disponible).</span><span class="sxs-lookup"><span data-stu-id="1f699-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="1f699-118">Los nombres de archivo de copia de seguridad tienen el formato Archive-*channelName* - *timestamp*. evtx y se encuentran en la carpeta% WINDIR% \\ system32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="1f699-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="1f699-119">**Tamañomáximo**</span><span class="sxs-lookup"><span data-stu-id="1f699-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="1f699-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="1f699-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="1f699-121">Tamaño máximo, en bytes, del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="1f699-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="1f699-122">El valor predeterminado (y el mínimo) es 1 MB.</span><span class="sxs-lookup"><span data-stu-id="1f699-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="1f699-123">Si el tamaño de registro físico es menor que el tamaño máximo configurado y se requiere espacio adicional en el registro para almacenar los eventos, el servicio asignará otro bloque de espacio aunque el tamaño físico resultante del registro sea mayor que el tamaño máximo configurado.</span><span class="sxs-lookup"><span data-stu-id="1f699-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="1f699-124">El servicio asigna bloques de 1 MB para que el tamaño físico pueda crecer hasta un máximo de 1 MB mayor que el tamaño máximo configurado.</span><span class="sxs-lookup"><span data-stu-id="1f699-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="1f699-125">**políticas**</span><span class="sxs-lookup"><span data-stu-id="1f699-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="1f699-126">boolean</span><span class="sxs-lookup"><span data-stu-id="1f699-126">boolean</span></span>                                                           | <span data-ttu-id="1f699-127">Determina si el archivo de registro es un archivo de registro secuencial o circular.</span><span class="sxs-lookup"><span data-stu-id="1f699-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="1f699-128">Establézcalo en **true** para un archivo de registro secuencial y en **false** para un archivo de registro circular.</span><span class="sxs-lookup"><span data-stu-id="1f699-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="1f699-129">El valor predeterminado es **false** para los tipos de canal operativo y de administración y **true** para los tipos de canal de depuración y análisis.</span><span class="sxs-lookup"><span data-stu-id="1f699-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="1f699-130">Para consultar un registro circular, primero debe deshabilitar el canal.</span><span class="sxs-lookup"><span data-stu-id="1f699-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="1f699-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f699-131">Remarks</span></span>

<span data-ttu-id="1f699-132">Puede especificar el atributo **MaxSize** para cualquier tipo de canal.</span><span class="sxs-lookup"><span data-stu-id="1f699-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="1f699-133">Solo puede especificar el atributo **AutoBackup** para los tipos de canal operativo y de administración.</span><span class="sxs-lookup"><span data-stu-id="1f699-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="1f699-134">Puede establecer el atributo de **retención** en falso (registro circular) para los tipos de canal operativo y de administración.</span><span class="sxs-lookup"><span data-stu-id="1f699-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="1f699-135">Puede establecer el atributo de **retención** en false (registro circular) para los tipos de canal analítico y de depuración, pero para ver los eventos en el visor de eventos de Windows, deberá deshabilitar primero el canal.</span><span class="sxs-lookup"><span data-stu-id="1f699-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="1f699-136">Tenga en cuenta que cuando se vuelve a habilitar el canal, los eventos se quitan del canal.</span><span class="sxs-lookup"><span data-stu-id="1f699-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f699-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f699-137">Requirements</span></span>



| <span data-ttu-id="1f699-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f699-138">Requirement</span></span> | <span data-ttu-id="1f699-139">Value</span><span class="sxs-lookup"><span data-stu-id="1f699-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f699-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f699-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1f699-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1f699-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f699-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f699-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1f699-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f699-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





