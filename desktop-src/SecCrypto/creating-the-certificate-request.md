---
description: El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Creación de la solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607ebbfd5d230c216c2b7ebc4d3b217e1f8c0d2a375d39cdd6b311ec145be361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768890"
---
# <a name="creating-the-certificate-request"></a>Creación de la solicitud de certificado

El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante. Normalmente, esto se realiza a través de algún tipo de interfaz de usuario (UI), aunque la información se puede tomar directamente de una base de datos sin necesidad de una interfaz de usuario. La directiva de la entidad de certificación (CA) establece el nivel [*de*](../secgloss/c-gly.md) información necesaria.

Un ejemplo de la información necesaria podría ser el siguiente:

-   Nombre común
-   Nombre de unidad
-   Nombre de la empresa
-   City (Ciudad)
-   Estado
-   País/región

> [!Note]  
> La interfaz está diseñada para realizar una única solicitud para cada instancia de xenroll. Debe crearse una instancia de xenroll independiente para crear cada [*solicitud de certificado.*](../secgloss/c-gly.md)

 

Para obtener información sobre cómo usar el Control de inscripción de certificados para solicitar un certificado en lenguajes de programación específicos, vea los temas siguientes:

-   [Ejemplo de solicitud en C++](request-sample-in-c-.md)
-   [Ejemplo de solicitud en VBScript](request-sample-in-vbscript.md)

 

 
