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
# <a name="establishing-communication-with-configuration-snap-ins"></a>Establecer la comunicación con los complementos de configuración

Una vez que la extensión del complemento de datos adjuntos se ha agregado al nodo servicios, debe establecer la comunicación con el complemento configuración de seguridad. Esto es necesario porque la extensión del complemento de datos adjuntos obtiene sus datos, así como cualquier cambio realizado por el usuario, desde el complemento configuración de seguridad. Esto se puede hacer tal y como se describe en el procedimiento siguiente.

**Para establecer la comunicación con los complementos de configuración de seguridad**

1.  Obtenga el nombre del archivo de configuración mediante \_ el \_ formato de Portapapeles de CCF SCESVC Attachment, que devuelve el nombre del archivo de configuración como un **PWSTR**.

    Si los datos adjuntos se insertan en un nodo de tipo de configuración, los datos adjuntos deben saber qué configuración es. (Comunica esta información a los complementos de configuración de seguridad durante la inicialización de la interfaz). En este caso, use el código siguiente.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Configure el contexto con los complementos de configuración de seguridad. Una vez conocido el nombre de configuración, o si el nodo de servicio es un nodo de análisis, la extensión del complemento de datos adjuntos debe llamar a [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para configurar el contexto, tal y como se muestra en el ejemplo siguiente.

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
> Cuando haya terminado de usar el identificador devuelto por [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), cierre el controlador mediante una llamada a la función [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) . Normalmente, esto se hace cuando el usuario cierra la consola MMC.

 

 

 



