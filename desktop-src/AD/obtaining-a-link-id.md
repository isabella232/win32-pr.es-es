---
title: Obtener un identificador de vínculo
description: A partir de Windows Server 2003, ya no es necesario solicitar un linkID de Microsoft; hay un proceso para generar automáticamente un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtener un identificador de vínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149173"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="adeca-104">Obtener un identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="adeca-104">Obtaining a Link ID</span></span>

<span data-ttu-id="adeca-105">A partir de Windows Server 2003, ya no es necesario solicitar un [**LinkId**](/windows/desktop/ADSchema/a-linkid) de Microsoft; hay un proceso para generar automáticamente un **LinkId**.</span><span class="sxs-lookup"><span data-stu-id="adeca-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="adeca-106">El sistema generará automáticamente un identificador de vínculo para un nuevo atributo vinculado cuando el atributo **LinkId** del atributo esté establecido en 1.2.840.113556.1.2.50.</span><span class="sxs-lookup"><span data-stu-id="adeca-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="adeca-107">Para crear un vínculo de retroceso para este vínculo de avance, establezca el **LinkId** en el [**attributeID**](/windows/desktop/ADSchema/a-attributeid) o [**LDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) del vínculo hacia delante.</span><span class="sxs-lookup"><span data-stu-id="adeca-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="adeca-108">La caché de esquema debe volver a cargarse después de crear el vínculo hacia delante y antes de crear el vínculo de retroceso.</span><span class="sxs-lookup"><span data-stu-id="adeca-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="adeca-109">De lo contrario, no se encontrará el **attributeId** o **LDAPDisplayName** del vínculo de reenvío cuando se cree el vínculo de retroceso.</span><span class="sxs-lookup"><span data-stu-id="adeca-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="adeca-110">La caché de esquema se recarga a petición, unos minutos después de que se realiza un cambio en el esquema o cuando se reinicia el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="adeca-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="adeca-111">Cree todos los vínculos hacia delante, vuelva a cargar la caché de esquema y, a continuación, cree todos los vínculos hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="adeca-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="adeca-112">Por ejemplo, si ha creado los nuevos atributos **myForwardLinkAttr** y **myBackLinkAttr**, y desea vincularlos:</span><span class="sxs-lookup"><span data-stu-id="adeca-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="adeca-113">Los OID de este ejemplo son inventado.</span><span class="sxs-lookup"><span data-stu-id="adeca-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="adeca-114">Consulte [obtención de un identificador de objeto de Microsoft](obtaining-an-object-identifier-from-microsoft.md) para obtener instrucciones sobre cómo obtener OID para nuevos atributos.</span><span class="sxs-lookup"><span data-stu-id="adeca-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="adeca-115">Establezca estos atributos en el atributo que va a ser el vínculo hacia delante:</span><span class="sxs-lookup"><span data-stu-id="adeca-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="adeca-116">Vuelva a cargar el esquema.</span><span class="sxs-lookup"><span data-stu-id="adeca-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="adeca-117">Establezca estos atributos en el atributo que va a ser el vínculo de retroceso:</span><span class="sxs-lookup"><span data-stu-id="adeca-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="adeca-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adeca-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adeca-119">Atributos vinculados</span><span class="sxs-lookup"><span data-stu-id="adeca-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="adeca-120">Cómo extender el esquema</span><span class="sxs-lookup"><span data-stu-id="adeca-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 