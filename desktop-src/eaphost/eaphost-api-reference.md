---
title: Referencia de API de EAPHost
description: Obtenga información sobre las API de EAPHost y sus componentes. Consulte la información de referencia de varios temas de la API, como el esquema XML de EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421396"
---
# <a name="eaphost-api-reference"></a>Referencia de API de EAPHost

Las API de EAPHost están divididas en tres componentes: las API de suplicante, a las que se puede llamar directamente desde una aplicación habilitada para EAP; las API del método EAP del mismo nivel, que administran solicitudes de suplicante para un tipo de autenticación EAP específico y generan elementos interactivos en el cliente. y las API del autenticador de EAP, que realizan la autenticación del lado servidor de un suplicante.

Los dos últimos componentes de la API: el método EAP del mismo nivel y las API del método de autenticador EAP: requieren una implementación personalizada y compatible en los archivos DLL que los exponen al servicio EAPHost. No se pueden llamar directamente desde el código de la aplicación; en su lugar, lo llaman EAPHost (en el lado cliente para los métodos EAP peer y en el lado servidor para los métodos de autenticación EAP) si la implementación coincide con las firmas de API especificadas en la documentación correspondiente. La información específica de la implementación de la API se proporciona en cada página de referencia de funciones.

## <a name="eaphost-registry-settings"></a>Configuración del registro de EAPHost



| Tema                                                      | Descripción                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [Configuración del registro de EAPHost](eaphost-registry-settings.md) | Describe las claves del registro utilizadas por EAPHost. |



 

## <a name="eaphost-xml-schema"></a>Esquema XML de EAPHost



| Tema                                            | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost y esquema heredado](eaphost-schemas.md) | Describe el esquema de EAPHost y el esquema heredado para crear el XML de configuración y el XML de credenciales. |



 

## <a name="common-eaphost-api-reference"></a>Referencia común de API de EAPHost



| Tema                                                                   | Descripción                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Enumeraciones comunes de la API de EAPHost](common-eap-host-api-enumerations.md) | Enumera las constantes comunes a todas las API de EAPHost.  |
| [Estructuras comunes de API de EAPHost](common-eap-host-api-structures.md)     | Enumera las estructuras comunes a todas las API de EAPHost. |
| [Constantes de API de EAPHost comunes](common-eap-host-error-constants.md)     | Enumera las constantes comunes a todas las API de EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Referencia de API de EAPHost



| Tema                                                                       | Descripción                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Referencia de API suplicante de EAPHost](eap-host-supplicant-api-reference.md)   | Describe los elementos de API disponibles para habilitar las llamadas de suplicante a EAPHost.                                                                      |
| [Referencia de API de método del mismo nivel de EAPHost](eap-host-peer-method-api-reference.md) | Describe los elementos de la API que se deben implementar para crear un archivo DLL de método EAP del mismo nivel que un cliente EAPHost puede cargar y llamar.          |
| [API del método de autenticador de EAPHost](eaphost-authenticator-method-apis.md)  | Describe los elementos de la API que se deben implementar para crear un archivo DLL de método de autenticación de EAP que se pueda cargar y llamar mediante un servidor EAPHost. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de EAPHost](about-eap-host.md)
</dt> <dt>

[Uso de EAPHost](using-eap-host.md)
</dt> </dl>

 

 




