---
title: Componente de kernel de DRM (desusado)
description: Componente de kernel de DRM (desusado)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- SDK de Windows Media Format, componente de kernel DRM
- Administración de derechos digitales (DRM), componente de kernel
- DRM (administración de derechos digitales), componente de kernel
- Microsoft Secure audio Path (SAP), componente de kernel de DRM
- Ruta de acceso de audio seguro (SAP), componente de kernel DRM
- SAP (ruta de acceso de audio seguro), componente de kernel DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078584"
---
# <a name="the-drm-kernel-component-deprecated"></a>Componente de kernel de DRM (desusado)

En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.

En el modelo de Microsoft Secure audio Path (SAP), el componente kernel de DRM proporciona dos características básicas que protegen la integridad de la música cifrada.

En primer lugar, el componente cliente DRM y el componente kernel DRM están en comunicación cuando se reproduce un archivo de música. Esta comunicación entre componentes impide que cualquier persona manipule la señal cifrada o inserte información falsa.

En segundo lugar, el componente de kernel DRM no descifra la señal de música hasta que se autentiquen todos los componentes restantes. Es decir, antes de descifrar el contenido y pasarlo al siguiente componente del sistema, el componente kernel de DRM comprueba cada componente que permanece en la ruta de acceso a la tarjeta de sonido (cada componente que puede tener acceso al contenido) y comprueba que estos componentes están firmados con un certificado de Microsoft. Un componente sin firmar podría indicar un componente sospechoso o un controlador malintencionado. Por lo tanto, cuando el componente de kernel DRM valida los componentes restantes, si alguno de los componentes produce un error en esta prueba, la señal se detiene y no se puede reproducir. De lo contrario, si todos los componentes pasan la validación, el componente kernel de DRM descifra la música y la pasa al componente siguiente.

Microsoft firma digitalmente los controladores que pasan las pruebas del laboratorio de calidad de hardware (WHQL) de Windows® para garantizar a los usuarios que usan los controladores de mayor calidad. Esta práctica es estándar y garantiza la autenticidad de los componentes, ya que no se puede falsificar la firma ni se puede modificar el código sin destruir la firma. Los controladores que están certificados para la ruta de acceso de audio segura deben proteger los datos de audio que procesan desde los componentes que no son de confianza. 

Los controladores incluidos con Windows Millennium Edition y Windows XP se actualizan para la ruta de acceso de audio segura y con la firma. Los controladores que no están firmados para su uso con Windows me o Windows XP no pueden reproducir música protegida. Los fabricantes de controladores pueden volver a emitir versiones actualizadas de sus controladores firmados por WHQL y publicarlos en Internet para que los consumidores lo descarguen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ruta de acceso de audio seguro de Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




