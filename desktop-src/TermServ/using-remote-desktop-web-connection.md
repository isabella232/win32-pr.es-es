---
title: Usar el control ActiveX Escritorio remoto
description: Cómo puede utilizar el control ActiveX Escritorio remoto para personalizar la experiencia del usuario Servicios de Escritorio remoto.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, usar Escritorio remoto control ActiveX
- Conexión web a Escritorio remoto Servicios de Escritorio remoto, usar
- Protocolo de escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685486"
---
# <a name="using-the-remote-desktop-activex-control"></a>Usar el control ActiveX Escritorio remoto

Los temas siguientes contienen información sobre cómo puede utilizar el control ActiveX Escritorio remoto para personalizar la experiencia del usuario Servicios de Escritorio remoto.

El control ActiveX Escritorio remoto está disponible en los siguientes formatos:

-   **El control Scriptable**: implementa interfaces que son seguras para el scripting. Esta forma de control la pueden usar los clientes Web o los hosts de scripting (como VBScript).
-   **El control que no admite scripts**: ofrece funcionalidad adicional que no es segura para el scripting. Este formulario del control se puede usar desde código nativo o administrado, pero los clientes Web o los hosts de scripting no pueden usar este formulario.

La lista siguiente contiene los **CLSID** para los diferentes controles de diferentes versiones de sistema operativo. Cada **CLSID** es compatible con versiones posteriores del sistema. Por ejemplo, el **CLSID** para el control con scripts en Windows Vista funcionará en versiones posteriores del sistema, como Windows 7.



| Versión del sistema                          | CLSID de control que admite scripts             | CLSID de control que no admite scripts          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8, Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista con Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Incrustar el control ActiveX Escritorio remoto en una página web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Ejemplo que muestra el uso de las interfaces que admiten scripts.

</dd> <dt>

[Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Ejemplos de código que muestran los pasos para implementar canales virtuales que admiten scripts con Conexión web a Escritorio remoto.

</dd> <dt>

[Usar el control ActiveX Escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente.

</dd> <dt>

[Página Web de ejemplo incluida con el control ActiveX Escritorio remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Una página web de ejemplo (Default.htm) está en el directorio donde está instalado Conexión web a Escritorio remoto.

</dd> <dt>

[Proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md)
</dt> <dd>

Algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.

</dd> <dt>

[Deshabilitar características de Servicios de Escritorio remoto](disabling-terminal-services-features.md)
</dt> <dd>

Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.

</dd> </dl>

Para obtener más información acerca de la Página Web de ejemplo que se incluye con la instalación del control ActiveX Escritorio remoto, vea [Página Web de ejemplo que se incluye con el control activex escritorio remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 




