---
title: Uso del control Escritorio remoto ActiveX control
description: Cómo puede usar el control Escritorio remoto ActiveX para personalizar la experiencia Servicios de Escritorio remoto usuario.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , mediante Escritorio remoto ActiveX control
- Conexión web a Escritorio remoto Servicios de Escritorio remoto , mediante
- Protocolo de escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249873"
---
# <a name="using-the-remote-desktop-activex-control"></a>Uso del control Escritorio remoto ActiveX control

Los temas siguientes contienen información sobre cómo puede usar el control Escritorio remoto ActiveX para personalizar la experiencia Servicios de Escritorio remoto usuario.

El control Escritorio remoto ActiveX está disponible en los siguientes formularios:

-   **El control que permite scripts:** implementa interfaces que son seguras para scripting. Los clientes web o los hosts de scripting (como VBScript) pueden usar esta forma del control.
-   **El control noscriptable** ofrece funcionalidad adicional que no es segura para el scripting. Esta forma del control se puede usar desde código nativo o administrado, pero los clientes web o los hosts de solo scripting no pueden usar este formulario.

La lista siguiente contiene los **CLSID** de los distintos controles para las distintas versiones del sistema operativo. Cada uno de los **CLSID** es compatible con versiones posteriores del sistema. Por ejemplo, el **CLSID** del control que permite scripts en Windows Vista funcionará en versiones posteriores del sistema, como Windows 7.



| Versión del sistema                          | CLSID de control que permite scripts             | CLSID de control noscriptable          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8, Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista con Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Inserción del control Escritorio remoto ActiveX en una página web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Ejemplo que muestra el uso de las interfaces que se pueden incluir en scripts.

</dd> <dt>

[Implementación de canales virtuales que pueden incluir scripts mediante Conexión web a Escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Ejemplos de código que muestran los pasos para implementar canales virtuales con scripts con Conexión web a Escritorio remoto.

</dd> <dt>

[Uso del control Escritorio remoto ActiveX con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Si ha habilitado una aplicación de canales virtuales en Servicios de Escritorio remoto implementación, puede hacer que esta aplicación esté disponible para los equipos cliente.

</dd> <dt>

[Página web de ejemplo incluida con el control Escritorio remoto ActiveX ejemplo](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Una página web de ejemplo (Default.htm) se encuentra en el directorio donde Conexión web a Escritorio remoto está instalado.

</dd> <dt>

[Proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md)
</dt> <dd>

Algunas propiedades del objeto Escritorio remoto ActiveX control están restringidas a zonas de seguridad Internet Explorer URL específicas.

</dd> <dt>

[Deshabilitación de Servicios de Escritorio remoto características](disabling-terminal-services-features.md)
</dt> <dd>

Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.

</dd> </dl>

Para obtener más información sobre la página web de ejemplo que se incluye con la instalación del control Escritorio remoto ActiveX, vea Página web de ejemplo incluida [con el control Escritorio remoto ActiveX .](sample-web-page-included-with-the-remote-desktop-activex-control.md)

 

 




