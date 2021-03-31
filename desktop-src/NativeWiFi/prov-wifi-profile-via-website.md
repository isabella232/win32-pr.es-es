---
title: Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web
description: Permita a los usuarios descargar un perfil de un sitio web y aprovisionarlo.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995602"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web

El flujo de trabajo que se describe en este tema se presentó en la versión 2004 de Windows 10. En este tema se muestra cómo configurar un sitio web para que un usuario pueda aprovisionar un perfil para una red Passpoint (o para una red normal) antes de pasar al alcance de los puntos de acceso de Wi-Fi correspondientes. Un escenario de ejemplo es el de un usuario que puede estar planeando visitar un aeropuerto o una conferencia por primera vez, y que quieren prepararse de antemano descargando y aprovisionando un perfil en casa.

Como desarrollador, puede habilitar el flujo de trabajo proporcionando un perfil XML y configurando un sitio Web. Después, los usuarios pueden aprovisionar un perfil de Wi-Fi descargándolo desde su sitio web a través de un explorador Web. En el dispositivo del usuario, el perfil de Wi-Fi se aprovisiona con la activación de URI y la aplicación de **configuración** de Windows.

Este flujo de trabajo sustituye al mecanismo de Internet Explorer para el aprovisionamiento de perfiles de Wi-Fi, que se basa en las API de JavaScript específicas de Microsoft. Se espera que este nuevo flujo de trabajo funcione con todos los exploradores principales.

## <a name="the-workflow-in-more-detail"></a>El flujo de trabajo con más detalle

Puede activar este flujo de trabajo desde un hipervínculo que incluya como argumento el URI de descarga del documento XML de aprovisionamiento.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Por ejemplo, el siguiente marcado HTML proporciona un vínculo para instalar los perfiles que se encuentran en un documento hipotético `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

El XML debe cumplir el esquema de aprovisionamiento (consulte [aprovisionamiento de cuentas](/windows-hardware/drivers/mobilebroadband/account-provisioning)). El XML también debe incluir uno o varios elementos [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .Cada perfil se mostrará en el cuadro de diálogo **Agregar** que se describe a continuación.

Cuando el usuario hace clic en el vínculo HTML, el flujo de trabajo de instalación se invoca en la aplicación de **configuración** . El documento XML de aprovisionamiento lo descarga la aplicación de **configuración** . Una vez descargado, se muestra información sobre los perfiles, la firma y el firmante (siempre que el documento se adhiera al esquema).

![La aplicación de configuración](images/install-dialog.png)

El botón **Agregar** del cuadro de diálogo de la aplicación **configuración** solo está habilitado si el archivo de aprovisionamiento está firmado y es de confianza.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>En la página web, determine si se admite este flujo de trabajo

No hay ninguna manera de que JavaScript determine la versión de compilación exacta de Windows. Pero si el usuario usa el explorador Web Microsoft Edge, puede determinar la versión de Edge mediante la inspección del valor del `User-agent` encabezado HTTP. Si la versión es mayor o igual que `18.nnnnn` , se admite el flujo de trabajo.

## <a name="related-topics"></a>Temas relacionados

* [Aprovisionamiento de cuentas](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Elemento WLANProfile](./wlan-profileschema-wlanprofile-element.md)