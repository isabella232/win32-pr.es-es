---
title: Revocación de licencia (cliente DRM de Microsoft Windows Media)
description: Revocación de licencia (cliente DRM de Microsoft Windows Media)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, revocación de licencia
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), revocación de licencia
- DRM (administración de derechos digitales), revocación de licencia
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, revocación de licencia
- API extendidas de cliente, revocación de licencia
- licencias, revocación
- revocación de licencias, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279734"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revocación de licencia (cliente DRM de Microsoft Windows Media)

La revocación de licencias hace referencia a la eliminación de licencias de un almacén de licencias local. Un escenario común para la revocación de licencias se produce cuando un proveedor de servicios, como un servicio de suscripción de música, debe desactivar el servicio en el equipo de un usuario.

Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias. La aplicación puede hospedar este servicio o puede ser una aplicación Web. En cualquier caso, la aplicación debe ser capaz de recibir un desafío de licencia creado por el servicio.

Para quitar licencias del almacén de licencias, haga lo siguiente:

1.  Tras recibir un desafío de licencia del emisor de la licencia, cree un desafío de revocación mediante el método [**IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) . Este método asignará un búfer que contiene los datos de un desafío de revocación, que se pasa a la aplicación a través del parámetro *ppbChallengeOutput* .
2.  Envíe el desafío de revocación de licencias a un servicio de revocación de licencias. El servidor generará un BLOB de revocación de licencias (LRB) en respuesta.
3.  Quite la licencia del almacén local mediante el método [**IWMDRMLicenseManagement::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , pasando el LRB devuelto por el servidor de licencias.
4.  Desasigne el búfer asignado por **CreateLicenseRevocationChallenge** mediante la función **CoTaskMemFree** .

Para obtener más información sobre cómo funciona la revocación de licencias o sobre cómo escribir un servicio de revocación, consulte implementación de la [revocación de licencias](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Almacén de licencias local**](local-license-store.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 