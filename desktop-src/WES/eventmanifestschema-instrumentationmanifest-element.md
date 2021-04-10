---
title: Elemento instrumentationManifest
description: Nodo raíz del manifiesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- elemento instrumentationManifest EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279893"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="56aa3-104">Elemento instrumentationManifest</span><span class="sxs-lookup"><span data-stu-id="56aa3-104">instrumentationManifest Element</span></span>

<span data-ttu-id="56aa3-105">Nodo raíz del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="56aa3-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="56aa3-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56aa3-106">Child elements</span></span>



| <span data-ttu-id="56aa3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="56aa3-107">Element</span></span>                                                                                        | <span data-ttu-id="56aa3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="56aa3-108">Type</span></span>                                                                               | <span data-ttu-id="56aa3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="56aa3-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56aa3-110">**instrumentación**</span><span class="sxs-lookup"><span data-stu-id="56aa3-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="56aa3-111">**InstrumentationType**</span><span class="sxs-lookup"><span data-stu-id="56aa3-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="56aa3-112">En esta sección se definen uno o varios proveedores de eventos y los eventos que registran.</span><span class="sxs-lookup"><span data-stu-id="56aa3-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="56aa3-113">**View**</span><span class="sxs-lookup"><span data-stu-id="56aa3-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="56aa3-114">**LocalizationType**</span><span class="sxs-lookup"><span data-stu-id="56aa3-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="56aa3-115">En esta sección se definen las cadenas de mensaje localizadas que los consumidores usan para la presentación.</span><span class="sxs-lookup"><span data-stu-id="56aa3-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="56aa3-116">Por ejemplo, esta sección contendría la cadena de mensaje localizada para el nombre del proveedor, los eventos que defina y los atributos de evento que defina, como canales, tareas y códigos de error.</span><span class="sxs-lookup"><span data-stu-id="56aa3-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="56aa3-117">**metadata**</span><span class="sxs-lookup"><span data-stu-id="56aa3-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="56aa3-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="56aa3-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="56aa3-119">En esta sección se definen los tipos de metadatos que pueden usar otros manifiestos.</span><span class="sxs-lookup"><span data-stu-id="56aa3-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="56aa3-120">Para obtener un ejemplo, vea el archivo Winmeta.xml incluido en la \\ carpeta include del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="56aa3-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="56aa3-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56aa3-121">Remarks</span></span>

<span data-ttu-id="56aa3-122">El elemento **instrumentationManifest** debe contener los espacios de nombres siguientes:</span><span class="sxs-lookup"><span data-stu-id="56aa3-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="56aa3-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="56aa3-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="56aa3-124">xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="56aa3-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="56aa3-125">xmlns: XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="56aa3-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="56aa3-126">Un manifiesto debe contener una sección de instrumentación y una sección de localización.</span><span class="sxs-lookup"><span data-stu-id="56aa3-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="56aa3-127">La sección de instrumentación y los metadatos se excluyen mutuamente (no puede definir ambos en el mismo manifiesto).</span><span class="sxs-lookup"><span data-stu-id="56aa3-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="56aa3-128">Aunque puede crear un manifiesto que contiene una sección de metadatos, el servicio no lo usará; los únicos metadatos que reconoce el servicio son los metadatos que se encuentran en el archivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="56aa3-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="56aa3-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56aa3-129">Examples</span></span>

<span data-ttu-id="56aa3-130">En el ejemplo siguiente se muestra el esqueleto de un manifiesto de instrumentación totalmente definido.</span><span class="sxs-lookup"><span data-stu-id="56aa3-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="56aa3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56aa3-131">Requirements</span></span>



| <span data-ttu-id="56aa3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="56aa3-132">Requirement</span></span> | <span data-ttu-id="56aa3-133">Value</span><span class="sxs-lookup"><span data-stu-id="56aa3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56aa3-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56aa3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="56aa3-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56aa3-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56aa3-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56aa3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="56aa3-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56aa3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





