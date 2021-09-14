---
description: El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Creación de la solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259508"
---
# <a name="creating-the-certificate-request"></a>Creación de la solicitud de certificado

El proceso de creación de una solicitud de certificado implica la recopilación de cierta información del solicitante. Normalmente, esto se realiza a través de algún tipo de interfaz de usuario (UI), aunque la información se podría tomar directamente de una base de datos sin necesidad de una interfaz de usuario. La directiva de la entidad de certificación (CA) establece el nivel [*de*](../secgloss/c-gly.md) información necesario.

Un ejemplo de la información necesaria podría ser el siguiente:

-   Nombre común
-   Nombre de unidad
-   Nombre de la empresa
-   City (Ciudad)
-   Estado
-   País/región

> [!Note]  
> La interfaz está diseñada para realizar una única solicitud para cada instancia de xenroll. Se debe crear una instancia de xenroll independiente para crear cada [*solicitud de certificado.*](../secgloss/c-gly.md)

 

Para obtener información sobre cómo usar el Control de inscripción de certificados para solicitar un certificado en lenguajes de programación específicos, vea los temas siguientes:

-   [Ejemplo de solicitud en C++](request-sample-in-c-.md)
-   [Ejemplo de solicitud en VBScript](request-sample-in-vbscript.md)

 

 
