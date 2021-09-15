---
title: Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web
description: Permitir a los usuarios descargar un perfil de un sitio web y aprovisionarlo.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566961"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web

El flujo de trabajo descrito en este tema se introdujo en Windows 10, versión 2004. En este tema se muestra cómo configurar un sitio web para que un usuario pueda aprovisionar un perfil para una red de punto de acceso (o para una red normal) antes de pasar al intervalo de los puntos de acceso de Wi-Fi correspondientes. Un escenario de ejemplo es el de un usuario que podría planear visitar un aeropuerto o una conferencia por primera vez, y quiere prepararse de antemano descargando y aprovisionando un perfil en casa.

Como desarrollador, puede habilitar el flujo de trabajo proporcionando un perfil XML y configurando un sitio web. A continuación, los usuarios pueden aprovisionar Wi-Fi perfil de usuario descargándose de su sitio web a través de un explorador web. En el dispositivo del usuario, el perfil de Wi-Fi se aprovisiona mediante la activación de URI y la Windows **Configuración** aplicación.

Este flujo de trabajo reemplaza el mecanismo de Internet Explorer para aprovisionar Wi-Fi perfiles, que se basa en las API de JavaScript específicas de Microsoft. Se espera que este nuevo flujo de trabajo funcione con todos los exploradores principales.

## <a name="the-workflow-in-more-detail"></a>Flujo de trabajo con más detalle

Puede activar este flujo de trabajo desde un hipervínculo que incluya como argumento el URI de descarga del documento XML de aprovisionamiento.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Por ejemplo, el siguiente marcado HTML proporciona un vínculo para instalar los perfiles que se encuentran en un documento hipotético `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

El XML debe cumplir el esquema de aprovisionamiento (vea [Aprovisionamiento de cuentas).](/windows-hardware/drivers/mobilebroadband/account-provisioning) El XML también debe incluir uno o varios [elementos WLANProfile.](./wlan-profileschema-wlanprofile-element.md) Cada perfil se mostrará en el cuadro **de** diálogo Agregar que se describe a continuación.

Cuando el usuario hace clic en el vínculo HTML, se invoca el flujo de trabajo de instalación en **Configuración** aplicación. El documento XML de aprovisionamiento se descarga mediante **Configuración** aplicación. Una vez descargado, se muestra información sobre los perfiles, la firma y el firmante (siempre que el documento cumpla el esquema).

![La Configuración aplicación](images/install-dialog.png)

El **botón** Agregar del cuadro de diálogo **de Configuración** aplicación solo está habilitado si el archivo de aprovisionamiento está firmado y es de confianza.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>En la página web, determine si se admite este flujo de trabajo.

No hay ninguna manera en JavaScript de determinar la versión de compilación exacta de Windows. Pero si el usuario usa el explorador web Microsoft Edge, puede determinar la versión de Edge inspeccionando el valor del `User-agent` encabezado HTTP. Si la versión es mayor o igual que `18.nnnnn` , se admite el flujo de trabajo.

## <a name="related-topics"></a>Temas relacionados

* [Aprovisionamiento de cuentas](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Elemento WLANProfile](./wlan-profileschema-wlanprofile-element.md)