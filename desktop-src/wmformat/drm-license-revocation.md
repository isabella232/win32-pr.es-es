---
title: Revocación de licencias (cliente DRM Windows Multimedia de Microsoft)
description: Revocación de licencias (cliente DRM Windows Multimedia de Microsoft)
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
- licenses,revocation
- revocación de licencias, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3cd295ddc1aec40c04f5284d791d7482854208a17875bdd3ed60d998f4ccf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027843"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revocación de licencias (cliente DRM Windows Multimedia de Microsoft)

La revocación de licencias hace referencia a la eliminación de licencias de un almacén de licencias local. Un escenario común para la revocación de licencias se produce cuando un proveedor de servicios, como un servicio de suscripción de música, debe desactivar el servicio en el equipo de un usuario.

El proceso de revocación de licencias lo inicia un servicio proporcionado por el emisor de la licencia. La aplicación puede hospedar este servicio o puede ser una aplicación web. En cualquier caso, la aplicación debe ser capaz de recibir un desafío de licencia creado por el servicio.

Para quitar licencias del almacén de licencias, haga lo siguiente:

1.  Tras recibir un desafío de licencia del emisor de licencias, cree un desafío de revocación mediante el método [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) Este método asignará un búfer que contiene datos de desafío de revocación, que se pasan a la aplicación a través del *parámetro ppbChallengeOutput.*
2.  Envíe el desafío de revocación de licencias a un servicio de revocación de licencias. El servidor generará un BLOB de revocación de licencias (LRB) en respuesta.
3.  Quite la licencia del almacén local mediante el método [**IWMDRMLicenseManagement::P rocessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) y pase el LRB devuelto por el servidor de licencias.
4.  Desasigne el búfer asignado por **CreateLicenseRevocationChallenge** mediante la **función CoTaskMemFree.**

Para obtener más información sobre cómo funciona la revocación de licencias o sobre cómo escribir un servicio de revocación, vea [Implementación de la revocación de licencias.](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Almacén de licencias local**](local-license-store.md)
</dt> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 