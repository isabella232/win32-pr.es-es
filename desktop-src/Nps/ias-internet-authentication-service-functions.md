---
title: Funciones de extensiones nps
description: Funciones de extensiones nps
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cecf8ead61e94287ba4846b82f922af40068a771a9bcadd8ccb51693709c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362365"
---
# <a name="nps-extensions-functions"></a>Funciones de extensiones nps

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

## <a name="application-defined"></a>Aplicación definida

La arquitectura de archivos DLL de extensión NPS admite las siguientes funciones exportadas:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Las [**funciones RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) [**y RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) son opcionales.

El archivo DLL de extensión [**puede exportar RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en lugar de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) [**o RadiusExtensionProcessEx.**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)

Si el archivo DLL de extensión [**exporta RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), también debe exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definido por el sistema

Cuando NPS llama a una implementación de [**RadiusExtensionProcess2,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)NPS pasa a la función un puntero a una [**estructura RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK.**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)

La [**estructura RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene punteros de función a las siguientes funciones proporcionadas por NPS:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Las funciones [**GetRequest**](/previous-versions/ms688263(v=vs.85)) y [**GetResponse**](/previous-versions/ms688270(v=vs.85)) devuelven punteros a una estructura de tipo [**RADIUS ATTRIBUTE \_ \_ ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

La [**estructura RADIUS ATTRIBUTE \_ \_ ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene punteros de función a las siguientes funciones proporcionadas por NPS:

-   [**Añadir**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 