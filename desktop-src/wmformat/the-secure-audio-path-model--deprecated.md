---
title: Modelo de ruta de acceso de audio segura (desusado)
description: Modelo de ruta de acceso de audio segura (desusado)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- Administración de derechos digitales (DRM), Microsoft Secure audio Path (SAP)
- DRM (administración de derechos digitales), Microsoft Secure audio Path (SAP)
- SDK de Windows Media Format, ruta de acceso de audio segura (SAP)
- Administración de derechos digitales (DRM), ruta de acceso de audio segura (SAP)
- DRM (administración de derechos digitales), ruta de acceso de audio segura (SAP)
- Microsoft Secure audio Path (SAP), modelo
- Ruta de acceso de audio seguro (SAP), modelo
- SAP (ruta de acceso segura de audio), modelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418597"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Modelo de ruta de acceso de audio segura (desusado)

En esta página se documenta una característica que se admitirá con una solución técnica diferente en versiones futuras de Windows.

Microsoft Secure audio Path (SAP) es una característica de Microsoft Windows® me y Microsoft Windows XP. El requisito de que se reproduzca un archivo de audio solo a través de una ruta de acceso de audio segura se especifica en la licencia de DRM y lo aplican los componentes de cliente DRM. No se agrega ningún cifrado adicional para los archivos solo de SAP cuando están protegidos inicialmente. Los componentes de DRM agregan automáticamente el cifrado de SAP en el momento de la reproducción, como es el proceso de autenticación para todos los componentes de software implicados en la reproducción. Por lo tanto, el funcionamiento de SAP es completamente transparente para las aplicaciones y, por eso, no hay ningún método o propiedad en el SDK de Windows Media Format para habilitar o deshabilitar SAP. Si lo desea, al crear un archivo protegido, el propietario del contenido puede Agregar un atributo de encabezado personalizado denominado algo como "DRMHeader. SAPRequired" para indicar a un servidor de licencias que agregue el requisito de SAP a la licencia. La implementación de este tipo de esquema depende del propietario del contenido y del servicio de licencias.

En el modelo DRM actual, si no se aplica SAP, cuando se reproduce la música digital protegida, el contenido cifrado pasa al componente cliente DRM. El cliente DRM comprueba que la aplicación y el componente DRM que incorpora el SDK de Windows Media Format son válidos. Si son válidos, el cliente DRM descifra el contenido y lo envía a la aplicación, que luego lo envía a los componentes de audio de nivel inferior. En este momento, la música descifrada está disponible para las aplicaciones en modo usuario y los complementos y controladores de modo kernel que pueden interceptar los bits de audio descifrados.

Cuando se aplica el requisito de la ruta de acceso de audio segura, la aplicación no descifra el contenido, sino que se pasa a un estado cifrado a los componentes de nivel inferior, que Microsoft ha autenticado como de confianza. Un componente de audio de confianza es aquél que no hace que el contenido de audio esté disponible para ningún componente del sistema, excepto otros componentes de confianza específicos. De esta manera, el contenido digital permanece protegido hasta el nivel del controlador.

En el diagrama siguiente se muestra el modelo actual en comparación con el modelo de ruta de acceso de audio segura.

![diagrama del modelo de ruta de acceso de audio segura](images/sap.png)

 

 




