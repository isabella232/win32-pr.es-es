---
title: Control de contenido protegido
description: Control de contenido protegido
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Administrador de dispositivos,certificates
- Administrador de dispositivos,certificates
- aplicaciones de escritorio, certificados
- proveedores de servicios, certificados
- guía de programación, certificados
- certificates
- Windows Proveedor Administrador de dispositivos contenido seguro (SCP)
- Administrador de dispositivos proveedor de contenido seguro (SCP)
- aplicaciones de escritorio, proveedor de contenido seguro (SCP)
- proveedores de servicios, proveedor de contenido seguro (SCP)
- guía de programación, proveedor de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Contenido Administrador de dispositivos multimedia protegido con DRM
- Administrador de dispositivos contenido protegido por DRM
- guía de programación, contenido protegido con DRM
- aplicaciones de escritorio, contenido protegido con DRM
- proveedores de servicios, contenido protegido por DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967851"
---
# <a name="handling-protected-content"></a>Control de contenido protegido

Si va a crear una aplicación o proveedor de servicios que consumirá contenido protegido por Windows Media Digital Rights Management (DRM), debe tener un par de claves y certificados emitido por Microsoft. Para obtener información sobre dónde obtener este certificado, consulte [Herramientas de desarrollo.](tools-for-development.md) Si no piensa controlar el contenido protegido, puede usar la clave ficticia y el certificado proporcionados con este SDK en un archivo denominado key.c.

Para cualquier archivo protegido por la tecnología DRM, Windows Media Administrador de dispositivos requiere la presencia de un proveedor de contenido seguro (SCP) para ese formato de archivo. Microsoft proporciona un módulo SCP para archivos WMA y WMV. Si su aplicación o proveedor de servicios va a controlar contenido protegido con DRM de otro formato, debe proporcionar su propio módulo SCP. Un módulo SCP es un objeto COM que implementa todas las interfaces para [los proveedores de contenido seguro.](interfaces-for-secure-content-providers.md)

Una aplicación puede enviar contenido protegido con DRM a dispositivos basados en Windows Media DRM 10 para dispositivos portátiles o DRM de dispositivos portátiles (PDDRM). Sin embargo, solo puede crear un proveedor de servicios para dispositivos basados en PDDRM; No puede crear un proveedor de servicios para dispositivos basados en Windows DRM 10 de multimedia para dispositivos portátiles. Estos últimos dispositivos solo pueden usar el proveedor de servicios MTP proporcionado por Microsoft.

Los dispositivos basados en PDDRM solo pueden admitir licencias para el contenido comprado. Las licencias que tienen condiciones de expiración de hora solo son compatibles con dispositivos basados en Windows Media DRM 10 para dispositivos portátiles, que tienen requisitos especiales, como un reloj seguro e individualización. Windows El SDK de DRM 10 multimedia para dispositivos portátiles proporciona detalles sobre los requisitos del dispositivo para admitir la tecnología de la versión 10.

Antes de enviar contenido DRM al dispositivo, una aplicación debe comprobar varias cosas:

-   Que el dispositivo admite la tecnología DRM.
-   Qué versión de la tecnología DRM admite (versión 10 o anterior).
-   Si el dispositivo se basa en la versión 10, todos sus componentes están actualizados (por ejemplo, el reloj seguro y los requisitos de individualización).

Todas las llamadas a métodos para responder a estas preguntas las realiza el cliente y se controlan mediante Windows Media Administrador de dispositivos y el componente del proveedor de contenido seguro. el proveedor de servicios no controla ninguna de estas llamadas.

Si el dispositivo no admite Windows Media DRM 10 para dispositivos portátiles, es posible que todavía pueda consumir contenido protegido (según la licencia de contenido y el diseño del dispositivo), pero cualquier contenido que se le envíe tendrá una licencia de uso simplificada con derechos limitados (por ejemplo, sin expiración de tiempo).

-   Para obtener ejemplos que muestran cómo una aplicación comprueba si un dispositivo puede controlar el contenido protegido y si necesita actualizar sus componentes DRM, consulte Control de contenido protegido en [la aplicación.](handling-protected-content-in-the-application.md)
-   Para obtener más información sobre cómo crear un proveedor de servicios que pueda controlar el contenido protegido, vea Control de [contenido protegido en el proveedor de servicios](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Muchos Windows métodos de solicitud de derechos o transferencia de archivos Administrador de dispositivos media media producirán un error (a menudo con un valor **HRESULT** incobranible) al controlar archivos protegidos con DRM con un depurador asociado. Por lo tanto, debe usar maneras alternativas de depurar el código, como registrar salidas en un formulario Windows o un archivo de registro. Para obtener más información sobre las opciones de registro, vea [Habilitación del registro.](enabling-logging.md) Si ejecuta un depurador en contenido protegido, un método devolverá uno de los códigos de error enumerados en la sección Códigos de error de DRM [o,](error-codes.md)posiblemente, un código de error desconocido. Si obtiene valores **HRESULT extraños** al ejecutar un depurador en métodos o contenido protegido, la protección DRM podría ser la causa.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




