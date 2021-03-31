---
title: Control de contenido protegido
description: Control de contenido protegido
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- aplicaciones de escritorio, certificados
- proveedores de servicios, certificados
- Guía de programación, certificados
- certificates
- Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- Administrador de dispositivos, proveedor de contenido seguro (SCP)
- aplicaciones de escritorio, proveedor de contenido seguro (SCP)
- proveedores de servicios, proveedor de contenido seguro (SCP)
- Guía de programación, proveedor de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- aplicaciones de escritorio, contenido protegido con DRM
- proveedores de servicios, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418561"
---
# <a name="handling-protected-content"></a>Control de contenido protegido

Si va a crear una aplicación o un proveedor de servicios que consume contenido protegido por la administración de derechos digitales (DRM) de Windows Media, debe tener un par de claves/certificados emitidos por Microsoft. Para obtener información sobre dónde obtener este certificado, vea [herramientas para el desarrollo](tools-for-development.md). Si no desea controlar el contenido protegido, puede usar la clave ficticia y el certificado proporcionado con este SDK en un archivo denominado Key. c.

En el caso de cualquier archivo que esté protegido por la tecnología DRM, Windows Media Administrador de dispositivos requiere la presencia de un proveedor de contenido seguro (SCP) para ese formato de archivo. Microsoft proporciona un módulo SCP para archivos WMA y WMV. Si su aplicación o proveedor de servicios va a controlar el contenido protegido con DRM de otro formato, debe proporcionar su propio módulo SCP. Un módulo SCP es un objeto COM que implementa todas las [interfaces para los proveedores de contenido seguros](interfaces-for-secure-content-providers.md).

Una aplicación puede enviar contenido protegido con DRM a dispositivos basados en Windows Media DRM 10 para dispositivos portátiles o DRM de dispositivo portátil (PDDRM). Sin embargo, solo puede crear un proveedor de servicios para dispositivos basados en PDDRM; no se puede crear un proveedor de servicios para dispositivos integrados en Windows Media DRM 10 para dispositivos portátiles. Estos últimos dispositivos solo pueden usar el proveedor de servicios MTP proporcionado por Microsoft.

Los dispositivos basados en PDDRM solo admiten licencias para contenido adquirido. Las licencias que tienen condiciones de expiración de tiempo solo se admiten en dispositivos basados en Windows Media DRM 10 para dispositivos portátiles, que tienen requisitos especiales, como un reloj seguro y una individualización. El SDK de Windows Media DRM 10 para dispositivos portátiles ofrece detalles sobre los requisitos de los dispositivos para admitir la tecnología de la versión 10.

Antes de enviar contenido DRM al dispositivo, una aplicación debe comprobar varias cosas:

-   Que el dispositivo admita la tecnología DRM.
-   Qué versión de la tecnología DRM es compatible (versión 10 o anterior).
-   Si el dispositivo se basa en la versión 10, todos sus componentes están actualizados (como el reloj seguro y los requisitos de individualización).

Todas las llamadas a métodos para responder a estas preguntas las realiza el cliente y las controla Windows Media Administrador de dispositivos y el componente de proveedor de contenido seguro. el proveedor de servicios no controla ninguna de estas llamadas.

Si el dispositivo no es compatible con DRM 10 de Windows Media para dispositivos portátiles, es posible que siga pudiendo consumir contenido protegido (en función de la licencia de contenido y el diseño del dispositivo), pero cualquier contenido que se le envíe tendrá una licencia de uso simplificada con derechos limitados (por ejemplo, sin expiración de tiempo).

-   Para obtener ejemplos en los que se muestra cómo una aplicación comprueba si un dispositivo puede controlar contenido protegido y si es necesario actualizar sus componentes de DRM, consulte [Administración del contenido protegido en la aplicación](handling-protected-content-in-the-application.md).
-   Para obtener más información acerca de la creación de un proveedor de servicios que pueda controlar el contenido protegido, consulte [control del contenido protegido en el proveedor de servicios](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Muchos métodos de transferencia de archivos de Windows Media Administrador de dispositivos o de solicitud de derechos producirán un error (a menudo con un valor **HRESULT** misterioso) al administrar archivos protegidos con DRM con un depurador adjunto. Por lo tanto, debe usar formas alternativas para depurar el código, como el registro de salidas en un archivo de registro o de Windows Forms. Para obtener más información sobre las opciones de registro, vea [Habilitar el registro](enabling-logging.md). Si está ejecutando un depurador en contenido protegido, un método devolverá uno de los códigos de error enumerados en los [códigos de error](error-codes.md)de la sección DRM o, posiblemente, un código de error desconocido. Si obtiene valores **HRESULT** misteriosas al ejecutar un depurador en métodos o contenido protegido, la protección DRM podría ser la causa.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




