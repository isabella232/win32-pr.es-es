---
description: El escenario de Access Control dinámica (DAC) permite la administración centralizada del control de acceso para escenarios de servidor de archivos empresariales.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Directiva de autorización centralizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003214"
---
# <a name="centralized-authorization-policy"></a>Directiva de autorización centralizada

El [escenario de Access Control dinámica (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) permite la administración centralizada del control de acceso para escenarios de servidor de archivos empresariales. La mayoría de las organizaciones tienen varias áreas en las que desean controlar el acceso.

Algunos ejemplos son:

-   Controlar el acceso a información confidencial, en la que los archivos marcados como confidenciales tendrán permisos específicos
-   Control del acceso a los archivos que contienen información de identificación personal (PII).
-   Limitar el acceso a los documentos en función de las directivas de retención de la organización.

Se proporcionan varias abstracciones nuevas de directiva de autorización para permitir que un Administrador defina estas directivas de forma centralizada y para simplificar el proceso de definición, ya que permite que cada uno de estos requisitos de acceso se definan y se mantengan por separado, pero se apliquen como una directiva.

Dos nuevos objetos de directiva de Active Directory, una [Directiva de autorización central](central-authorization-policies.md) (Cap) y una [regla de directiva de autorización central](central-authorization-policy-rule.md) (CAPR) se introdujeron en Windows 8 para definir y aplicar directivas de autorización centralizadas basadas en expresiones de notificaciones y atributos de recursos. al utilizar estos objetos, un administrador define un CAPR como una directiva de autorización específica que se puede aplicar a los recursos que tienen un atributo determinado o cumplen una determinada condición de aplicabilidad. por ejemplo, documentos etiquetados como "gran impacto para la empresa". se pueden definir CAPES para cada directiva de control de acceso deseada en una organización que se puede expresar y los recursos a los que se debe aplicar se pueden identificar, en términos de expresiones DAC de Windows 8. un extremo es una colección de caprs que se puede aplicar conjuntamente en los recursos. en el diagrama siguiente se muestran las relaciones entre el Cap y el cabo, así como los pasos conceptuales necesarios para definir y aplicar estos objetos a los recursos de archivo. ![relación de CAPES y Cap](images/cap.png)

 

 
