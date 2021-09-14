---
description: Ejemplo de certificado. Cree aplicaciones para la certificación de API, instale el certificado SSL, el certificado de servidor, cree un certificado a través de medios, como Internet o una intranet, que no sean intrínsecamente seguros.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de inscripción de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069042"
---
# <a name="certificate-enrollment-api"></a>API de inscripción de certificado

## <a name="purpose"></a>Propósito

La API de inscripción de certificados se puede usar para crear una aplicación cliente para solicitar un certificado e instalar una respuesta de certificado. Esta API se implementa en CertEnroll.dll a partir de Windows Vista; reemplaza a Xenroll.dll.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de inscripción de certificados es para que la usen los desarrolladores de aplicaciones que permitirán a los usuarios crear, solicitar y recuperar certificados a través de medios, como Internet o una intranet, que no son intrínsecamente seguros. Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++, el modelo de objetos componentes (COM) y el Windows de programación basado en componentes. Aunque no es necesario, se recomienda comprender la criptografía y la infraestructura de clave pública.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de inscripción de certificados se admite a partir de Windows Server 2008 y Windows Vista. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)<br/> | Se analizan los conceptos clave sobre las solicitudes de certificado.<br/>                                                                                                      |
| [Uso de la API de inscripción de certificados](using-the-certificate-enrollment-api.md)<br/> | Cómo usar la API de inscripción de certificados para ampliar las funcionalidades de Servicios de certificados de Active Directory.<br/>                                              |
| [Referencia de api de inscripción de certificados](certificate-enrollment-api-reference.md)<br/> | Descripciones detalladas de interfaces, enumeraciones y otros elementos de programación que se pueden usar para inscribir un usuario o equipo en una jerarquía de certificados.<br/> |



 

 

 




