---
title: Funciones de extensiones de NPS
description: Funciones de extensiones de NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685772"
---
# <a name="nps-extensions-functions"></a>Funciones de extensiones de NPS

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

## <a name="application-defined"></a>Aplicación definida

La arquitectura de los archivos dll de extensión NPS admite las siguientes funciones exportadas:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Las funciones [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) y [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) son opcionales.

El archivo DLL de extensión puede exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en lugar de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) o [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Si el archivo DLL de extensión exporta [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), también debe exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Definido por el sistema

Cuando NPS llama a una implementación de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS pasa la función a un puntero a una estructura de bloque de [**control de \_ extensión \_ \_ RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .

La estructura de [**\_ bloque de \_ control \_ de extensión RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene punteros de función a las siguientes funciones proporcionadas por NPS:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Las funciones [**GetRequest**](/previous-versions/ms688263(v=vs.85)) y [**GetResponse**](/previous-versions/ms688270(v=vs.85)) devuelven punteros a una estructura de tipo [**\_ \_ matriz de atributos RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

La estructura de la [**\_ \_ matriz de atributos RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene punteros de función a las siguientes funciones proporcionadas por NPS:

-   [**Agréguela**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize (**](/previous-versions/ms688277(v=vs.85))
-   [**Insertat (**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 