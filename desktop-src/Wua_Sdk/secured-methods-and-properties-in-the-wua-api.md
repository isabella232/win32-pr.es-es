---
description: Cuando WUA detecta que un llamador no tiene permiso para obtener acceso a una interfaz, método o propiedad, \_ se devuelve el ACCESSDENIED HRESULT.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Protección de interfaces, métodos y propiedades en la API de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696566"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Protección de interfaces, métodos y propiedades en la API de WUA

Algunas interfaces, métodos y propiedades de Windows Update Agent (WUA) son accesibles únicamente a los autores de llamadas que pertenecen a los siguientes grupos de seguridad de Windows:

-   Administrador
-   User (Usuario)
-   Usuario avanzado

Cuando WUA detecta que un llamador no tiene permiso para obtener acceso a una interfaz, método o propiedad,  \_ se devuelve el ACCESSDENIED HRESULT.

Las siguientes interfaces están disponibles para los grupos de seguridad de administrador, usuario y usuario avanzado:

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) y [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Si se cumplen las condiciones siguientes, se produce un error en la búsqueda:
>
> -   Un usuario que no es administrador establece la [**propiedad UserLocale de la interfaz IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) en una configuración regional que corresponde a un idioma que no está instalado en el equipo.
> -   La búsqueda usa un objeto UpdateSearch creado a partir del objeto UpdateSession.

 

Las siguientes interfaces de descarga y métodos están disponibles para los grupos de administradores y usuarios avanzados:

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden llamar a [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

Las siguientes interfaces de instalación, métodos y propiedades están disponibles para los grupos de administradores:

-   [**IAutomaticUpdates::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Propiedad IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden). Sin embargo, solo los administradores y los usuarios avanzados pueden establecer los valores.

     

-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Los administradores y los usuarios avanzados pueden llamar al [**método AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).

     

-   [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Propiedad NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel). Sin embargo, solo los administradores pueden establecer los valores.

     

-   [**Propiedad ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday). Sin embargo, solo los administradores pueden establecer los valores.

     

-   [**Propiedad ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Sin embargo, solo los administradores pueden establecer los valores.

     

-   [**Propiedad IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates). Sin embargo, solo los administradores pueden establecer los valores.

     

 

 



