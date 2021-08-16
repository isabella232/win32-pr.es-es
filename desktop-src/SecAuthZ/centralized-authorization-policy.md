---
description: El escenario de Access Control dinámica (DAC) permite la administración centralizada del control de acceso para escenarios de servidor de archivos empresariales.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Directiva de autorización centralizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a07730bff997b545285b0d2845547a4d5deaffe78324e354e7eecbf879b763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783198"
---
# <a name="centralized-authorization-policy"></a>Directiva de autorización centralizada

El [escenario de Access Control dinámica (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) permite la administración centralizada del control de acceso para escenarios de servidor de archivos empresariales. La mayoría de las organizaciones tienen varias áreas en las que quieren controlar el acceso.

Algunos ejemplos son:

-   Controlar el acceso a información confidencial, en la que los archivos marcados como confidenciales tendrían permisos específicos
-   Controlar el acceso a los archivos que contienen información de identificación personal (PII).
-   Limitar el acceso a los documentos en función de las directivas de retención de las organizaciones.

Se proporcionan varias abstracciones de directivas de autorización nuevas para permitir que un administrador defina estas directivas de forma centralizada y simplificar el proceso de definición al permitir que cada uno de estos requisitos de acceso se defina y mantenga por separado, pero se aplique como una directiva.

En Windows 8 se presentan dos nuevos objetos de directiva de Active Directory, una directiva de autorización [central](central-authorization-policies.md) (cap) y una regla de directiva de autorización [central](central-authorization-policy-rule.md) (capr) para definir y aplicar directivas de autorización centralizadas basadas en expresiones de notificaciones y atributos de recursos. al usar estos objetos, un administrador define un límite como una directiva de autorización específica que se puede aplicar a los recursos que tienen un atributo determinado o cumplen una condición de aplicabilidad determinada. por ejemplo, documentos etiquetados como "alto impacto empresarial". Se pueden definir capas para cada directiva de control de acceso deseada de una organización que se pueda expresar, y se pueden identificar los recursos a los que se debe aplicar, en términos de expresiones dac de Windows 8. un límite es una colección de caprs que se pueden aplicar juntos en los recursos. En el diagrama siguiente se muestran las relaciones entre el extremo y el cabo, y los pasos conceptuales implicados en la definición y aplicación de estos objetos a los recursos de archivo. ![relación de capas y límites](images/cap.png)

 

 
