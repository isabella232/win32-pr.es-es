---
description: Ejemplo de certificado. Cree aplicaciones para la certificación de API, instale el certificado SSL, el certificado de servidor, cree un certificado a través de medios, como Internet o una intranet, que no son intrínsecamente seguros.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de inscripción de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541806"
---
# <a name="certificate-enrollment-api"></a>API de inscripción de certificado

## <a name="purpose"></a>Propósito

La API de inscripción de certificados se puede usar para crear una aplicación cliente para solicitar un certificado e instalar una respuesta de certificado. Esta API se implementa en CertEnroll.dll a partir de Windows Vista; reemplaza Xenroll.dll.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de inscripción de certificados es para su uso por parte de desarrolladores de aplicaciones que permitirán a los usuarios crear, solicitar y recuperar certificados a través de medios, como Internet o una intranet, que no son intrínsecamente seguros. Los desarrolladores deben estar familiarizados con los lenguajes de programación de C y C++, el modelo de objetos componentes (COM) y el entorno de programación basado en Windows. Aunque no es necesario, se recomienda comprender la infraestructura de clave pública y criptografía.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de inscripción de certificados se admite a partir de Windows Server 2008 y Windows Vista. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la API de inscripción de certificados](about-the-certificate-enrollment-api.md)<br/> | Se describen los conceptos clave de las solicitudes de certificados.<br/>                                                                                                      |
| [Uso de la API de inscripción de certificados](using-the-certificate-enrollment-api.md)<br/> | Cómo usar la API de inscripción de certificados para ampliar las capacidades de Active Directory servicios de Certificate Server.<br/>                                              |
| [Referencia de API de inscripción de certificados](certificate-enrollment-api-reference.md)<br/> | Descripciones detalladas de las interfaces, las enumeraciones y otros elementos de programación que se pueden usar para inscribir un usuario o un equipo en una jerarquía de certificados.<br/> |



 

 

 




