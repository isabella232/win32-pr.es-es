---
title: Referencia de API de EAPHost
description: Obtenga información sobre las API de EAPHost y sus componentes. Consulte la información de referencia de varios temas de API, como el esquema XML de EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465741"
---
# <a name="eaphost-api-reference"></a>Referencia de API de EAPHost

Las API de EAPHost se dividen en tres componentes: las API suplicantes, a las que se puede llamar directamente desde una aplicación habilitada para EAP; las API del método del mismo nivel de EAP, que administran solicitudes suplicantes para un tipo de autenticación EAP específico y elevan elementos interactivos en el cliente; y las API de autenticación eap, que realizan la autenticación del lado servidor de un suplicante.

Los dos últimos componentes de LA API (el método del mismo nivel de EAP y las API de métodos de eap Authenticator) requieren una implementación personalizada y compatible en archivos DLL que los exponen al servicio EAPHost. No se pueden llamar directamente desde el código de la aplicación; En su lugar, EAPHost llama a ellos (en el lado cliente para los métodos del mismo nivel de EAP y en el lado servidor para los métodos autenticadores de EAP) si la implementación coincide con las firmas de API especificadas en la documentación correspondiente. La información específica de la implementación de la API se proporciona en cada página de referencia de función.

## <a name="eaphost-registry-settings"></a>EapHost Registry Configuración



| Tema                                                      | Descripción                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [EapHost Registry Configuración](eaphost-registry-settings.md) | Describe las claves del Registro consumidas por EAPHost. |



 

## <a name="eaphost-xml-schema"></a>Esquema XML de EAPHost



| Tema                                            | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost y esquema heredado](eaphost-schemas.md) | Describe el esquema EAPHost y el esquema heredado para crear XML de configuración y XML de credenciales. |



 

## <a name="common-eaphost-api-reference"></a>Referencia común de LA API de EAPHost



| Tema                                                                   | Descripción                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Enumeraciones comunes de API de EAPHost](common-eap-host-api-enumerations.md) | Enumera las constantes comunes a todas las API de EAPHost.  |
| [Estructuras comunes de API de EAPHost](common-eap-host-api-structures.md)     | Enumera las estructuras comunes a todas las API de EAPHost. |
| [Constantes comunes de LA API de EAPHost](common-eap-host-error-constants.md)     | Enumera las constantes comunes a todas las API de EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Referencia de API de EAPHost



| Tema                                                                       | Descripción                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Referencia de API de eaphost supplicant](eap-host-supplicant-api-reference.md)   | Describe los elementos de API disponibles para habilitar llamadas suplicantes a EAPHost.                                                                      |
| [Referencia de API del método del mismo nivel de EAPHost](eap-host-peer-method-api-reference.md) | Describe los elementos de API que se deben implementar para crear un archivo DLL de método del mismo nivel eap que un cliente EAPHost puede cargar y llamar.          |
| [API del método Authenticator EAPHost](eaphost-authenticator-method-apis.md)  | Describe los elementos de API que se deben implementar para crear un archivo DLL de método autenticador eap que un servidor EAPHost pueda cargar y llamar. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de EAPHost](about-eap-host.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> </dl>

 

 




