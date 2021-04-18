---
description: Una vez que la extensión del complemento de datos adjuntos se ha agregado al nodo servicios, debe establecer la comunicación con el complemento configuración de seguridad.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Establecer la comunicación con los complementos de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668012"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="73069-103">Establecer la comunicación con los complementos de configuración</span><span class="sxs-lookup"><span data-stu-id="73069-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="73069-104">Una vez que la extensión del complemento de datos adjuntos se ha agregado al nodo servicios, debe establecer la comunicación con el complemento configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73069-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="73069-105">Esto es necesario porque la extensión del complemento de datos adjuntos obtiene sus datos, así como cualquier cambio realizado por el usuario, desde el complemento configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73069-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="73069-106">Esto se puede hacer tal y como se describe en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="73069-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="73069-107">**Para establecer la comunicación con los complementos de configuración de seguridad**</span><span class="sxs-lookup"><span data-stu-id="73069-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="73069-108">Obtenga el nombre del archivo de configuración mediante \_ el \_ formato de Portapapeles de CCF SCESVC Attachment, que devuelve el nombre del archivo de configuración como un **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="73069-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="73069-109">Si los datos adjuntos se insertan en un nodo de tipo de configuración, los datos adjuntos deben saber qué configuración es.</span><span class="sxs-lookup"><span data-stu-id="73069-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="73069-110">(Comunica esta información a los complementos de configuración de seguridad durante la inicialización de la interfaz). En este caso, use el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="73069-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="73069-111">Configure el contexto con los complementos de configuración de seguridad. Una vez conocido el nombre de configuración, o si el nodo de servicio es un nodo de análisis, la extensión del complemento de datos adjuntos debe llamar a [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para configurar el contexto, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="73069-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> <span data-ttu-id="73069-112">Cuando haya terminado de usar el identificador devuelto por [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), cierre el controlador mediante una llamada a la función [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="73069-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="73069-113">Normalmente, esto se hace cuando el usuario cierra la consola MMC.</span><span class="sxs-lookup"><span data-stu-id="73069-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 



