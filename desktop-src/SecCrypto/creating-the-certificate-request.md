---
description: El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Crear la solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666420"
---
# <a name="creating-the-certificate-request"></a>Crear la solicitud de certificado

El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante. Normalmente, esto se realiza a través de algún tipo de interfaz de usuario, aunque la información podría tomarse directamente desde una base de datos sin necesidad de una interfaz de usuario. El nivel de la información requerida se establece mediante la Directiva de la entidad de [*certificación*](../secgloss/c-gly.md) (CA).

A continuación se muestra un ejemplo de la información necesaria:

-   Nombre común
-   Nombre de unidad
-   Nombre de la empresa
-   City (Ciudad)
-   Estado
-   País/región

> [!Note]  
> La interfaz está diseñada para hacer una solicitud única para cada instancia de XENROLL. Se debe crear una instancia de XENROLL independiente para crear cada [*solicitud de certificado*](../secgloss/c-gly.md).

 

Para obtener información sobre cómo usar el control de inscripción de certificados para solicitar un certificado en lenguajes de programación específicos, vea los temas siguientes:

-   [Ejemplo de solicitud en C++](request-sample-in-c-.md)
-   [Ejemplo de solicitud en VBScript](request-sample-in-vbscript.md)

 

 
