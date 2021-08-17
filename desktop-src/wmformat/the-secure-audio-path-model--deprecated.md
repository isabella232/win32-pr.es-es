---
title: Modelo de ruta de acceso de audio seguro (en desuso)
description: Modelo de ruta de acceso de audio seguro (en desuso)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows SDK de formato multimedia, ruta de acceso de audio seguro de Microsoft (SAP)
- digital rights management (DRM),Microsoft Secure Audio Path (SAP)
- DRM (administración de derechos digitales),Ruta de acceso de audio seguro de Microsoft (SAP)
- Windows SDK de formato multimedia, ruta de acceso de audio seguro (SAP)
- digital rights management (DRM), Secure Audio Path (SAP)
- DRM (administración de derechos digitales),Secure Audio Path (SAP)
- Ruta de acceso de audio seguro (SAP) de Microsoft, modelo
- Secure Audio Path (SAP),model
- SAP (Secure Audio Path),model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a381d29bcbf4b09ae989325cd5b35c332a6f316c1f932868437ac93a7854ab58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084295"
---
# <a name="the-secure-audio-path-model-deprecated"></a>Modelo de ruta de acceso de audio seguro (en desuso)

En esta página se documenta una característica que será compatible con otra solución técnica en versiones futuras de Windows.

Microsoft Secure Audio Path (SAP) es una característica de Microsoft Windows® Me y Microsoft Windows XP. El requisito de reproducir un archivo de audio solo a través de una ruta de acceso de audio segura se especifica en la licencia DRM y lo aplican los componentes de cliente DRM. No se agrega ningún cifrado adicional para los archivos solo de SAP cuando se protegen inicialmente. Los componentes de DRM agregan automáticamente el cifrado de SAP en el momento de la reproducción, al igual que el proceso de autenticación de todos los componentes de software implicados en la reproducción. Por lo tanto, el funcionamiento de SAP es completamente transparente para las aplicaciones y por eso no hay ningún método o propiedad en el SDK de formato multimedia de Windows para habilitar o deshabilitar SAP. Si lo desea, al crear un archivo protegido, un propietario de contenido puede agregar un atributo de encabezado personalizado denominado "DRMHeader.SAPRequired" para indicar a un servidor de licencias que agregue el requisito de SAP a la licencia. La implementación de este esquema es del propietario del contenido y del servicio de licencia.

En el modelo DRM actual, si no se aplica SAP, cuando se reproduce música digital protegida, el contenido cifrado pasa al componente de cliente DRM. El cliente DRM comprueba que la aplicación y el componente DRM que incorpora Windows SDK de formato multimedia son válidos. Si son válidos, el cliente DRM descifra el contenido y lo envía a la aplicación, que luego lo envía a los componentes de audio de nivel inferior. En este momento, la música descifrada está disponible para aplicaciones en modo de usuario y complementos y controladores de modo kernel que pueden interceptar los bits de audio descifrados.

Cuando se aplica el requisito de ruta de acceso de audio seguro, la aplicación no descifra el contenido, sino que se pasa en un estado cifrado a los componentes de nivel inferior, todos ellos autenticados por Microsoft como de confianza. Un componente de audio de confianza es aquel que no hace que el contenido de audio esté disponible para ningún componente del sistema, excepto para otros componentes de confianza específicos. De esta manera, el contenido digital permanece protegido hasta el nivel de controlador.

En el diagrama siguiente se muestra el modelo actual en comparación con el modelo de ruta de acceso de audio seguro.

![diagrama del modelo de ruta de acceso de audio segura](images/sap.png)

 

 




