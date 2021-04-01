---
title: Tipo complejo de ImportChannelType
description: Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- ImportChannelType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150247"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="c2794-104">Tipo complejo de ImportChannelType</span><span class="sxs-lookup"><span data-stu-id="c2794-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="c2794-105">Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c2794-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="c2794-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2794-106">Attributes</span></span>



| <span data-ttu-id="c2794-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2794-107">Name</span></span>   | <span data-ttu-id="c2794-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2794-108">Type</span></span>                                                              | <span data-ttu-id="c2794-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2794-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2794-110">chid</span><span class="sxs-lookup"><span data-stu-id="c2794-110">chid</span></span>   | <span data-ttu-id="c2794-111">token</span><span class="sxs-lookup"><span data-stu-id="c2794-111">token</span></span>                                                             | <span data-ttu-id="c2794-112">Identificador que identifica de forma única el canal en la lista de canales que el proveedor define o importa.</span><span class="sxs-lookup"><span data-stu-id="c2794-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="c2794-113">Use este valor cuando haga referencia a este canal en una definición de evento.</span><span class="sxs-lookup"><span data-stu-id="c2794-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="c2794-114">Si no especifica un identificador de canal, utilice el nombre del canal para hacer referencia a este canal en una definición de evento.</span><span class="sxs-lookup"><span data-stu-id="c2794-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="c2794-115">name</span><span class="sxs-lookup"><span data-stu-id="c2794-115">name</span></span>   | <span data-ttu-id="c2794-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="c2794-116">anyURI</span></span>                                                            | <span data-ttu-id="c2794-117">Nombre del canal que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="c2794-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c2794-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="c2794-118">symbol</span></span> | [<span data-ttu-id="c2794-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="c2794-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="c2794-120">Símbolo que se va a usar para hacer referencia al canal en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2794-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="c2794-121">El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el canal en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="c2794-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="c2794-122">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c2794-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c2794-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2794-123">Remarks</span></span>

<span data-ttu-id="c2794-124">El manifiesto que definió el canal importado debe instalarse antes de que el proveedor escriba eventos; de lo contrario, los eventos no se pueden escribir en el canal (la operación de escritura se realiza correctamente, los eventos simplemente no se escriben en el canal).</span><span class="sxs-lookup"><span data-stu-id="c2794-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2794-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2794-125">Requirements</span></span>



| <span data-ttu-id="c2794-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2794-126">Requirement</span></span> | <span data-ttu-id="c2794-127">Value</span><span class="sxs-lookup"><span data-stu-id="c2794-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c2794-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2794-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2794-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2794-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c2794-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2794-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2794-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2794-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





