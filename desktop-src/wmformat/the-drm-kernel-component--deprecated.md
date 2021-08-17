---
title: El componente de kernel drm (en desuso)
description: El componente de kernel drm (en desuso)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows SDK de formato multimedia, ruta de acceso de audio seguro de Microsoft (SAP)
- administración de derechos digitales (DRM),Ruta de acceso de audio seguro de Microsoft (SAP)
- DRM (administración de derechos digitales),Ruta de acceso de audio seguro de Microsoft (SAP)
- Windows SDK de formato multimedia, ruta de acceso de audio seguro (SAP)
- administración de derechos digitales (DRM),Ruta de acceso de audio seguro (SAP)
- DRM (administración de derechos digitales),Ruta de acceso de audio seguro (SAP)
- Windows SDK de formato multimedia, componente de kernel de DRM
- administración de derechos digitales (DRM), componente de kernel
- DRM (administración de derechos digitales), componente de kernel
- Ruta de acceso de audio seguro de Microsoft (SAP), componente de kernel drm
- Secure Audio Path (SAP), componente de kernel drm
- SAP (ruta de acceso de audio seguro), componente de kernel drm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845762"
---
# <a name="the-drm-kernel-component-deprecated"></a>El componente de kernel drm (en desuso)

En esta página se documenta una característica que será compatible con otra solución técnica en versiones futuras de Windows.

En el modelo de Microsoft Secure Audio Path (SAP), el componente de kernel DRM proporciona dos características básicas que protegen la integridad de la música cifrada.

En primer lugar, el componente de cliente DRM y el componente de kernel drm están en comunicación cuando se reproduce un archivo de música. Esta comunicación entre los componentes impide que alguien manipule la señal cifrada o inserte información falsa.

En segundo lugar, el componente de kernel drm no descifra la señal de música hasta que se autentican todos los componentes restantes. Es decir, antes de descifrar el contenido y pasarlo al siguiente componente del sistema, el componente de kernel DRM comprueba cada componente que permanece en la ruta de acceso a la tarjeta de sonido (cada componente que puede acceder al contenido) y comprueba que estos componentes están firmados con un certificado de Microsoft. Un componente sin signo puede indicar un componente sospechoso o un controlador malintencionado. Por lo tanto, cuando el componente de kernel DRM valida los componentes restantes, si algún componente no realiza esta prueba, la señal se detiene y no se puede reproducir. De lo contrario, si todos los componentes pasan la validación, el componente de kernel drm descifra la música y la pasa al componente siguiente.

Microsoft firma digitalmente los controladores que pasan las pruebas de Windows® Hardware Quality Lab (WHQL) para garantizar a los usuarios que usan los controladores de la más alta calidad. Esta práctica es estándar y garantiza la autenticidad de los componentes porque no se puede falsificación la firma ni se puede modificar el código sin destruir la firma. Los controladores que están certificados para Secure Audio Path deben proteger los datos de audio que procesan del acceso por parte de componentes que no son de confianza. 

Los controladores incluidos con Windows Millennium Edition y Windows XP se actualizan para Secure Audio Path y se firman. Los controladores que no están firmados para su uso con Windows o Windows XP no pueden reproducir música protegida. Los fabricantes de controladores pueden volver a emitir versiones actualizadas de sus controladores firmadas por WHQL y publicarlas en Internet para que los consumidores las descarguen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ruta de acceso de audio seguro de Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




