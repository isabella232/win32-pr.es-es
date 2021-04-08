---
title: Usar el manifiesto de transferencia
description: El Asistente para publicación web y el Asistente para la ordenación de impresión en línea utilizan el manifiesto de transferencia para comunicar detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Asistente para publicación Web, transferir manifiesto
- Asistente para orden de impresión en línea, transferir manifiesto
- transferir manifiesto
- manifest
- Window. external, transferir manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904595"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="7be9b-108">Usar el manifiesto de transferencia</span><span class="sxs-lookup"><span data-stu-id="7be9b-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="7be9b-109">El Asistente para publicación web y el Asistente para la ordenación de impresión en línea utilizan el manifiesto de transferencia para comunicar detalles de la transferencia de datos entre el equipo cliente y el sitio del servidor.</span><span class="sxs-lookup"><span data-stu-id="7be9b-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="7be9b-110">El propósito del manifiesto de transferencia</span><span class="sxs-lookup"><span data-stu-id="7be9b-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="7be9b-111">El manifiesto de transferencia describe los archivos implicados en la transferencia, incluidos los detalles como la jerarquía de destino y los metadatos del archivo.</span><span class="sxs-lookup"><span data-stu-id="7be9b-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="7be9b-112">El script de servidor puede modificar el manifiesto quitando archivos inadecuados de la lista y agregando información sobre cómo y dónde se deben transferir los archivos.</span><span class="sxs-lookup"><span data-stu-id="7be9b-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="7be9b-113">El manifiesto se expone como la propiedad **window. external. Property ("TransferManifest")**, un documento de Document Object Model XML (dom).</span><span class="sxs-lookup"><span data-stu-id="7be9b-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="7be9b-114">Para obtener más información acerca del DOM XML, vea la documentación de MSDN para [IXMLDOMDocument/DomDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7be9b-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="7be9b-115">La organización de nivel superior del manifiesto de transferencia es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7be9b-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="7be9b-116">La página HTML del lado servidor puede usar los nodos del manifiesto para obtener cierta información sobre los archivos que se van a copiar y, a continuación, modificar la interfaz de usuario del servicio en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="7be9b-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="7be9b-117">Por ejemplo, un sitio de impresión fotográfica podría usar la información para mostrar vistas en miniatura de las imágenes elegidas, mientras que un sitio de almacenamiento podría usar la información para asegurarse de que hay suficiente espacio de almacenamiento disponible para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="7be9b-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="7be9b-118">Para obtener información completa sobre los atributos y nodos del manifiesto de transferencia, vea [transferir el esquema del manifiesto](/windows/desktop/shell/interfaces).</span><span class="sxs-lookup"><span data-stu-id="7be9b-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="7be9b-119">El esquema de manifiesto de transferencia se escribe como un modelo abierto para que los elementos no definidos específicamente en el esquema puedan aparecer en el manifiesto de transferencia.</span><span class="sxs-lookup"><span data-stu-id="7be9b-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="7be9b-120">Por lo tanto, un sitio de proveedor podría agregar elementos propietarios para su propio uso sin alterar la validez del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="7be9b-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="7be9b-121">También se define el esquema para que el orden de los elementos no esté restringido.</span><span class="sxs-lookup"><span data-stu-id="7be9b-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="7be9b-122">El manifiesto se vuelve a crear cada vez que se elige un proveedor nuevo para que el proveedor tenga la oportunidad de almacenar información del sitio en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="7be9b-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7be9b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7be9b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7be9b-124">Transferir esquema de manifiesto</span><span class="sxs-lookup"><span data-stu-id="7be9b-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 