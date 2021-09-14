---
title: Revocación de licencias (cliente DRM de Microsoft Windows Media)
description: Revocación de licencias (cliente DRM de Microsoft Windows Media)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows SDK de formato multimedia, licencias
- Windows SDK de formato multimedia, revocación de licencias
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), revocación de licencias
- DRM (administración de derechos digitales), revocación de licencias
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, revocación de licencias
- API extendidas de cliente, revocación de licencias
- licencias, revocación
- revocación de licencias, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359576"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revocación de licencias (cliente DRM de Microsoft Windows Media)

La revocación de licencias hace referencia a la eliminación de licencias de un almacén de licencias local. Un escenario común de revocación de licencias se produce cuando un proveedor de servicios, como un servicio de suscripción de música, debe desactivar el servicio en el equipo de un usuario.

Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias. La aplicación puede hospedar este servicio o puede ser una aplicación web. En cualquier caso, la aplicación debe poder recibir un desafío de licencia creado por el servicio.

Para quitar licencias del almacén de licencias, haga lo siguiente:

1.  Tras recibir un desafío de licencia del emisor de licencias, cree un desafío de revocación mediante el método [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) Este método asignará un búfer que contiene datos de desafío de revocación, que se pasan a la aplicación a través del *parámetro ppbChallengeOutput.*
2.  Envíe el desafío de revocación de licencias a un servicio de revocación de licencias. El servidor generará un BLOB de revocación de licencias (LRB) en respuesta.
3.  Quite la licencia del almacén local mediante el método [**IWMDRMLicenseManagement::P rocessLicenseRevocationResponse,**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) pasando el LRB devuelto por el servidor de licencias.
4.  Desasigne el búfer asignado por **CreateLicenseRevocationChallenge** mediante la **función CoTaskMemFree.**

Para obtener más información sobre cómo funciona la revocación de licencias o sobre cómo escribir un servicio de revocación, vea [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Almacén de licencias local**](local-license-store.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 