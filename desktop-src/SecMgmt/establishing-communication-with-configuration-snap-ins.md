---
description: Después de que la extensión de complemento de datos adjuntos se haya agregado al nodo Servicios, debe establecer comunicación con el complemento Configuración de seguridad.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Establecimiento de la comunicación con complementos de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf186936f0b0ad21dc871a91e78dd0bbead04a0683450992e5e3b7dd7c516abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969403"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Establecimiento de la comunicación con complementos de configuración

Después de que la extensión de complemento de datos adjuntos se haya agregado al nodo Servicios, debe establecer comunicación con el complemento Configuración de seguridad. Esto es necesario porque la extensión de complemento de datos adjuntos obtiene sus datos, así como los cambios realizados por el usuario, desde el complemento Configuración de seguridad. Esto se puede hacer como se describe en el procedimiento siguiente.

**Para establecer la comunicación con los complementos de configuración de seguridad**

1.  Obtenga el nombre del archivo de configuración mediante el formato de Portapapeles \_ CCF SCESVC ATTACHMENT, que devuelve el nombre del archivo de configuración \_ como **PWSTR**.

    Si los datos adjuntos se insertan en un nodo de tipo de configuración, los datos adjuntos deben saber qué configuración es. (Comunica esta información a los complementos de configuración de seguridad durante la inicialización de la interfaz). En este caso, use el código siguiente.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Configure el contexto con los complementos configuración de seguridad. Una vez conocido el nombre de configuración, o si el nodo de servicio es un nodo de análisis, la extensión de complemento de datos adjuntos debe llamar a [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para configurar el contexto, como se muestra en el ejemplo siguiente.

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
> Cuando haya terminado de usar el identificador devuelto por [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), cierre el identificador mediante una llamada a la función [**ISceSvcAttachmentData::CloseHandle.**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) Esto suele hacerse cuando el usuario cierra la consola de MMC.

 

 

 



